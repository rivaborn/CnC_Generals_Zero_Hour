# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SimpleObjectIterator.cpp

## Purpose
Implements a simple linked-list based iterator for game objects with numeric values, supporting sorting.

## Responsibilities
- Manages a linked list of object-numeric pairs (Clumps)
- Provides iteration over objects with optional numeric values
- Supports sorting objects by various criteria (distance, cost)
- Handles memory cleanup of the iterator

## Key Types
- **SimpleObjectIterator (Class)**: Main iterator class managing object list and sorting
- **Clump (Struct)**: Node in linked list storing an Object and numeric value
- **ClumpCompareProc (typedef)**: Function pointer type for comparison functions
- **IterOrderType (enum)**: Sorting order types (near/far, cheap/expensive)

## Key Functions
### `insert(Object *obj, Real numeric)`
- Purpose: Adds an object with numeric value to the iterator
- Calls: `newInstance`

### `nextWithNumeric(Real *num)`
- Purpose: Returns next object in iteration with optional numeric value
- Calls: None

### `sort(IterOrderType order)`
- Purpose: Sorts objects using merge sort algorithm with specified comparison
- Calls: `theClumpCompareProcs[order]`, `reset()`

### `sortNearToFar/FarToNear/CheapToExpensive/ExpensiveToCheap(Clump *a, Clump *b)`
- Purpose: Comparison functions for different sorting orders
- Calls: `getTemplate()->friend_getBuildCost()` (for cost sorts)

## Globals
- **theClumpCompareProcs (ClumpCompareProc[])**: Array mapping sort types to comparison functions

## Dependencies
- `ObjectIter.h`, `ThingTemplate.h`, `Object.h`
- Uses `DEBUG_ASSERTCRASH`, `DEBUG_LOG` macros
- Depends on `Object` class and its template system
