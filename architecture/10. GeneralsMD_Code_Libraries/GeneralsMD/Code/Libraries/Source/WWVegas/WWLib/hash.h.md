# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hash.h

## Purpose
Defines a hash table implementation for string-based key-value lookups.

## Responsibilities
- Provides a hash table class for storing and retrieving objects by string keys
- Supports iteration over hash table entries
- Manages hash collisions via chaining
- Allows adding, removing, and finding entries

## Key Types
- **HashableClass (Class)**: Base class for objects that can be stored in the hash table; requires implementing Get_Key()
- **HashTableClass (Class)**: Main hash table implementation with add/remove/find operations
- **HashTableIteratorClass (Class)**: Iterator for traversing hash table entries

## Key Functions
### HashTableClass::Add
- Purpose: Adds an entry to the hash table
- Calls: Hash()

### HashTableClass::Find
- Purpose: Finds an entry by its key
- Calls: Hash()

### HashTableClass::Hash
- Purpose: Computes hash value for a string key
- Calls: None

### HashTableIteratorClass::First
- Purpose: Initializes iteration to the first entry
- Calls: Advance_Next()

### HashTableIteratorClass::Next
- Purpose: Advances to the next entry
- Calls: Advance_Next()

### HashTableIteratorClass::Advance_Next
- Purpose: Internal helper to advance to next valid entry
- Calls: None

## Globals
None

## Dependencies
- Key includes: "always.h"
- External symbols: None
