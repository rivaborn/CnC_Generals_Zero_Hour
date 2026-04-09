# Generals/Code/Libraries/Source/WWVegas/WWLib/hashtemplate.h

## Purpose
Implements a generic hash table template class for key-value storage.

## Responsibilities
- Provides hash table operations (insert, remove, lookup)
- Manages dynamic resizing and rehashing
- Supports iteration over entries
- Includes specialized hash functions for common types

## Key Types
- **HashTemplateKeyClass (Class)**: Provides hash value computation for keys
- **HashTemplateClass (Class)**: Main hash table implementation
- **Entry (Struct)**: Represents a hash table entry (key, value, next pointer)
- **(anonymous enum) (Enum)**: Defines NIL constant for null links
- **NIL (Enum)**: Represents null link in hash chains
- **HashTemplateIterator (Class)**: Iterates over hash table entries

## Key Functions
### HashTemplateClass::Insert
- Purpose: Adds a key-value pair to the hash table
- Calls: Alloc_Entry, Get_Hash_Val

### HashTemplateClass::Remove
- Purpose: Removes entries matching a key (or key-value pair)
- Calls: Get_Hash_Val

### HashTemplateClass::Get
- Purpose: Retrieves value for a given key
- Calls: Get_Hash_Val

### HashTemplateClass::Re_Hash
- Purpose: Resizes and rehashes the table when needed
- Calls: Get_Hash_Val, W3DNEWARRAY

### HashTemplateIterator::First/Next
- Purpose: Navigates through hash table entries
- Calls: HashTable.Get_Hash, HashTable.Get_Table

## Globals
None

## Dependencies
- Key includes: "always.h", "wwstring.h"
- External symbols: W3DNEWARRAY, StringClass
- Uses memory allocation/deallocation operators
