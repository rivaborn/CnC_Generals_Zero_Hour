# Generals/Code/Tools/matchbot/wlib/arraylist.h

## Purpose
Dynamic array-based list implementation with manual memory management for C++ objects.

## Responsibilities
- Manages a resizable array of objects with copy semantics
- Provides insertion, removal, and access operations
- Handles object construction/destruction via placement new
- Supports sorted insertion and binary search
- Optimizes memory usage via grow/shrink operations

## Key Types
- **ArrayList (Class)**: Generic container for managing a dynamic array of objects
- **(anonymous enum)**: Contains INITIAL_SIZE constant
- **INITIAL_SIZE (Enum)**: Default initial capacity (10)

## Key Functions
### ArrayList::add
- Purpose: Inserts an object at specified position
- Calls: growVector, memmove, placement new

### ArrayList::remove
- Purpose: Removes object at specified position
- Calls: destructor, memmove, shrinkVector

### ArrayList::addSortedAsc/Des
- Purpose: Inserts object while maintaining sorted order
- Calls: _sortedLookup, add

### ArrayList::growVector/shrinkVector
- Purpose: Resizes internal storage by 2x
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
