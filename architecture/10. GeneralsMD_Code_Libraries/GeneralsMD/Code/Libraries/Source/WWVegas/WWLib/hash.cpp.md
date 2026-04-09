# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hash.cpp

## Purpose
Implements a hash table data structure for storing and retrieving objects by string keys.

## Responsibilities
- Manages hash table creation, insertion, removal, and lookup
- Provides iteration over hash table entries
- Uses CRC-based hashing for key distribution

## Key Types
- **HashTableClass (Class)**: Manages the hash table storage and operations
- **HashableClass (Class)**: Abstract base for objects stored in the hash table
- **HashTableIteratorClass (Class)**: Iterates through hash table entries

## Key Functions
### `HashTableClass::Add`
- Purpose: Adds an entry to the hash table
- Calls: `Hash`, `WWASSERT`

### `HashTableClass::Remove`
- Purpose: Removes an entry from the hash table
- Calls: `Hash`, `WWASSERT`

### `HashTableClass::Find`
- Purpose: Finds an entry by key
- Calls: `Hash`, `stricmp`

### `HashTableClass::Hash`
- Purpose: Computes hash index for a key
- Calls: `CRC_Stringi`

### `HashTableIteratorClass::First`
- Purpose: Initializes iteration to first entry
- Calls: `Advance_Next`, `Next`

### `HashTableIteratorClass::Next`
- Purpose: Advances to next entry
- Calls: `Advance_Next`

## Globals
None

## Dependencies
- `hash.h`, `wwdebug.h`, `realcrc.h`, `osdep.h` (Unix only)
- `W3DNEWARRAY`, `WWASSERT` macros
- `CRC_Stringi` function
- `stricmp` function
