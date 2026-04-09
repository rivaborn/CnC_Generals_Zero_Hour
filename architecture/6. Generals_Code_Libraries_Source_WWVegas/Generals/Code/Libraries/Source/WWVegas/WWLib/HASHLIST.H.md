# Generals/Code/Libraries/Source/WWVegas/WWLib/HASHLIST.H

## Purpose
Implements a hash table with doubly-linked list functionality for efficient record storage and retrieval.

## Responsibilities
- Provides hash table operations (add, find, remove)
- Manages doubly-linked list of all records
- Supports user-defined node data via template
- Handles hash collisions with chaining
- Tracks node state (new record, in list, etc.)

## Key Types
- `HashListClass<T,U,N>` (Class): Main hash list container
- `HashNodeClass<T,U>` (Class): Individual node storing record and key
- `HashDefaultUserClass` (Class): Default empty user data class
- `HashNodeFriendClass<T,U>` (Class): Helper for internal node access

## Key Functions
### `Add(T record, unsigned key)`
- Purpose: Adds a record to the hash list creating a new node
- Calls: `W3DNEW`, `Add(HashNodeClass *)`

### `Add(HashNodeClass<T,U> *node)`
- Purpose: Adds an existing node to the hash list
- Calls: `Hash_Value()`, `Set_In_List()`, `Link()`, `Add_Head()`, `Set_First()`, `Set_Last()`

### `Find(unsigned key)`
- Purpose: Finds a record by its hash key
- Calls: `Hash_Value()`

### `Remove(HashNodeClass<T,U> *node)`
- Purpose: Removes a node from the hash list
- Calls: `Hash_Value()`, `Clear_First()`, `Clear_Last()`, `Clear_In_List()`, `Unlink()`

### `Move_To(HashListClass<T,U> *newlist)`
- Purpose: Moves all nodes to another hash list
- Calls: `First_Valid()`, `Next_Valid()`, `Clear_List_Created()`, `Remove()`, `Add()`, `Set_List_Created()`

## Globals
- `A_LARGE_PRIME_NUMBER` (const int): Default hash table size (257)

## Dependencies
- `listnode.h` (List/DataNode templates)
- `<memory.h>` (memset)
- `W3DNEW` macro (memory allocation)
