# Generals/Code/Tools/mangler/wlib/dictionary.h

## Purpose
Implements a hash dictionary template for fast key-value lookups using hashing.

## Responsibilities
- Provides hash-based key-value storage and retrieval
- Manages dynamic resizing (shrink/expand) of the hash table
- Supports iteration, insertion, deletion, and value updates
- Handles collision resolution via linked lists

## Key Types
- **DNode<K,V> (Class)**: Node structure containing key, value, and next pointer for hash collisions
- **Dictionary<K,V> (Class)**: Main hash dictionary class managing the table and operations

## Key Functions
### Dictionary::add
- Purpose: Adds or updates a key-value pair in the dictionary
- Calls: remove, keyHash, expand

### Dictionary::remove
- Purpose: Removes a key-value pair by key
- Calls: keyHash, shrink

### Dictionary::getValue
- Purpose: Retrieves a value by key
- Calls: getPointer

### Dictionary::shrink
- Purpose: Reduces table size by half when underutilized
- Calls: keyHash

### Dictionary::expand
- Purpose: Doubles table size when overutilized
- Calls: keyHash

## Globals
- **SHRINK_THRESHOLD (const double)**: Threshold (0.20) for shrinking the table
- **EXPAND_THRESHOLD (const double)**: Threshold (0.80) for expanding the table
- **MIN_TABLE_SIZE (const int)**: Minimum table size (128)

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<assert.h>`
- `wstypes.h` (for types like `uint32`, `bit8`)
- Uses `new`/`delete` for memory management
