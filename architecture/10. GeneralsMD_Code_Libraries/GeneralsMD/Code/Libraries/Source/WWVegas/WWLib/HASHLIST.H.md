# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/HASHLIST.H

## Purpose
This file defines a hash table implementation with linked list functionality, allowing efficient record storage and retrieval.

## Responsibilities
- Provides a templated hash list class for storing and retrieving records by key
- Manages collisions via linked lists within hash buckets
- Supports node creation/deletion and list operations
- Tracks node state with flags (new record, in list, etc.)

## Key Types
- `HashDefaultUserClass` (class): Default empty user data class for nodes
- `HashNodeClass<T,U>` (template class): Node containing record, key, and flags
- `HashNodeFriendClass<T,U>` (template class): Friend class for internal node access
- `HashListClass<T,U,NumHashValues>` (template class): Main hash list container

## Key Functions
### `HashListClass::Add(T record, unsigned key)`
- Purpose: Adds a record to the hash list with automatic node creation
- Calls: `W3DNEW`, `HashListClass::Add(HashNodeClass *)`

### `HashListClass::Find(unsigned key)`
- Purpose: Searches for a record by key in the hash table
- Calls: `Hash_Value()`, `Is_Last()`

### `HashListClass::Remove(HashNodeClass<T,U> *node)`
- Purpose: Removes a node from the hash list
- Calls: `Hash_Value()`, `Is_First()`, `Is_Last()`, `Clear_First()`, `Clear_Last()`, `Clear_In_List()`, `Unlink()`

### `HashListClass::Move_To(HashListClass<T,U> *newlist)`
- Purpose: Moves all nodes from one list to another
- Calls: `First_Valid()`, `Next_Valid()`, `Is_List_Created()`, `Clear_List_Created()`, `Remove()`, `Add()`

## Globals
- `A_LARGE_PRIME_NUMBER` (const int): Default hash table size (257)

## Dependencies
- `listnode.h` (List/DataNode templates)
- `<memory.h>` (memset)
- `W3DNEW` macro (memory allocation)
