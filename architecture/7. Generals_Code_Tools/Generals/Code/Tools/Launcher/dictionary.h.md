# Generals/Code/Tools/Launcher/dictionary.h

## Purpose
Implements a hash dictionary template for fast key-value lookups using hashing.

## Responsibilities
- Provides a generic hash table with dynamic resizing
- Supports insertion, lookup, deletion, and iteration
- Manages memory for nodes and table
- Handles collisions via chaining

## Key Types
- **DNode<K,V> (Class)**: Node structure holding key, value, and next pointer
- **Dictionary<K,V> (Class)**: Hash table container with resizing logic

## Key Functions
### Dictionary::add
- Purpose: Inserts or updates a key-value pair
- Calls: `remove`, `keyHash`, `expand`

### Dictionary::getValue
- Purpose: Retrieves value by key
- Calls: `keyHash`

### Dictionary::remove
- Purpose: Deletes a key-value pair
- Calls: `keyHash`, `shrink`

### Dictionary::shrink/expand
- Purpose: Resizes table when load factor thresholds are crossed
- Calls: `keyHash`

## Globals
- **MIN_TABLE_SIZE (const int)**: Minimum table size (32)
- **SHRINK_THRESHOLD (const double)**: Shrink trigger (0.20)
- **EXPAND_THRESHOLD (const double)**: Expand trigger (0.80)

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<assert.h>`
- `wstypes.h`, `wdebug.h`
- Uses `bit8`, `uint32`, `sint32` types
