# Generals/Code/Tools/mangler/wlib/arraylist.h

## Purpose
Template-based dynamic array implementation for list operations with manual memory management.

## Responsibilities
- Provides dynamic array storage for arbitrary types
- Supports insertion, removal, and retrieval at arbitrary positions
- Manages memory growth/shrinkage automatically
- Handles object construction/destruction via placement new
- Offers sorted insertion variants

## Key Types
- **ArrayList (Class)**: Dynamic array container with list operations
- **(anonymous enum)**: Contains INITIAL_SIZE constant
- **INITIAL_SIZE (Enum)**: Initial allocation size (10)

## Key Functions
### ArrayList::add
- Purpose: Inserts an element at specified position
- Calls: growVector, memmove, placement new

### ArrayList::remove
- Purpose: Removes element at specified position
- Calls: destructor, memmove, shrinkVector

### ArrayList::addSortedAsc/addSortedDes
- Purpose: Inserts element maintaining sorted order
- Calls: _sortedLookup, add

### ArrayList::growVector/shrinkVector
- Purpose: Expands/contracts underlying storage
- Calls: new, memcpy, delete[]

### ArrayList::_sortedLookup
- Purpose: Binary search for sorted insertion position
- Calls: getPointer

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<assert.h>`, `<new.h>`, `<math.h>`
- `wstypes.h` (for bit8, sint32, uint8 types)
- Uses placement new and manual destructor calls
