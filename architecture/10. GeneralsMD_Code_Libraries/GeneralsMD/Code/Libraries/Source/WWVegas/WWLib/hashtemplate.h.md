# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hashtemplate.h

## Purpose
Implements a generic hash table template class for key-value storage with iteration support.

## Responsibilities
- Provides hash table operations (insert, remove, lookup)
- Manages dynamic resizing and rehashing
- Supports iteration over entries
- Includes specialized hash functions for different key types

## Key Types
- **HashTemplateKeyClass (Class)**: Provides hash value computation for keys
- **HashTemplateClass (Class)**: Main hash table implementation
- **Entry (Struct)**: Represents a hash table entry (key, value, next pointer)
- **(anonymous enum) (Enum)**: Defines NIL constant for null links
- **NIL (Enum)**: Represents null link value (-1)
- **HashTemplateIterator (Class)**: Iterator for traversing hash table entries

## Key Functions
### HashTemplateClass::Insert
- Purpose: Adds a new key-value pair to the hash table
- Calls: Alloc_Entry, Get_Hash_Val

### HashTemplateClass::Set_Value
- Purpose: Sets value for existing key or inserts new pair
- Calls: Get_Hash_Val

### HashTemplateClass::Remove
- Purpose: Removes entry by key
- Calls: Get_Hash_Val

### HashTemplateClass::Re_Hash
- Purpose: Resizes and rehashes the table when needed
- Calls: Get_Hash_Val, W3DNEWARRAY

### HashTemplateIterator::First
- Purpose: Initializes iterator to first non-empty bucket
- Calls: HashTable.Get_Hash, HashTable.Get_Size

### HashTemplateIterator::Next
- Purpose: Advances iterator to next entry
- Calls: HashTable.Get_Table, HashTable.Get_Hash, HashTable.Get_Size

## Globals
None

## Dependencies
- "always.h"
- "wwstring.h"
- W3DNEWARRAY (memory allocation)
- StringClass (for specialized hash function)
