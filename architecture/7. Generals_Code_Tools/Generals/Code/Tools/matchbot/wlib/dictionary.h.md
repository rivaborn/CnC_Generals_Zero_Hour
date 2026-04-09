# Generals/Code/Tools/matchbot/wlib/dictionary.h

## Purpose
Implements a hash dictionary template for fast key-value lookups using hashing.

## Responsibilities
- Provides hash-based key-value storage and retrieval
- Manages dynamic resizing (shrink/expand) based on load thresholds
- Supports iteration, insertion, deletion, and value updates
- Handles memory allocation/deallocation for nodes and table

## Key Types
- **DNode (Class)**: Node structure containing key, value, and next pointer for hash collisions
- **Dictionary (Class)**: Main hash dictionary class with template parameters for key and value types

## Key Functions
### Dictionary::add
- Purpose: Adds or updates a key-value pair in the dictionary
- Calls: remove, keyHash, expand

### Dictionary::remove
- Purpose: Removes a key-value pair from the dictionary
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
- **SHRINK_THRESHOLD (const double)**: Load threshold (20%) for shrinking
- **EXPAND_THRESHOLD (const double)**: Load threshold (80%) for expanding
- **MIN_TABLE_SIZE (const int)**: Minimum table size (128)

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<assert.h>`
- `wstypes.h` (for bit8, uint32, etc.)
- Uses custom hash function provided by caller
