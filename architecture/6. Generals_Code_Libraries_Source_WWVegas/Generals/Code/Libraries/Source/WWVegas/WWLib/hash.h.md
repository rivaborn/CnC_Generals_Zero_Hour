# Generals/Code/Libraries/Source/WWVegas/WWLib/hash.h

## Purpose
Defines a hash table implementation for string-based key-value lookups.

## Responsibilities
- Provides a hash table class for storing hashable objects
- Supports adding, removing, and finding entries by string key
- Includes an iterator for traversing hash table entries
- Manages hash table resizing and collision handling

## Key Types
- **HashableClass (Class)**: Abstract base class for objects that can be stored in the hash table
- **HashTableClass (Class)**: Main hash table implementation
- **HashTableIteratorClass (Class)**: Iterator for traversing hash table entries

## Key Functions
### HashTableClass::Add
- Purpose: Adds an entry to the hash table
- Calls: Hash()

### HashTableClass::Find
- Purpose: Finds an entry by its string key
- Calls: Hash()

### HashTableClass::Hash
- Purpose: Converts a string key to a table index
- Calls: None

### HashTableIteratorClass::First
- Purpose: Initializes iteration to the first entry
- Calls: Advance_Next()

### HashTableIteratorClass::Next
- Purpose: Advances to the next entry
- Calls: Advance_Next()

### HashTableIteratorClass::Advance_Next
- Purpose: Internal method to advance to next valid entry
- Calls: None

## Globals
- None

## Dependencies
- Key includes: "always.h"
- External symbols: None
