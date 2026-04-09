# GeneralsMD/Code/GameEngine/Include/GameLogic/ObjectIter.h

## Purpose
Defines iterator classes for traversing collections of game objects.

## Responsibilities
- Provides abstract base class `ObjectIterator` for object iteration.
- Implements `SimpleObjectIterator` with sorting capabilities.
- Manages object iteration with memory pooling and deletion handling.

## Key Types
- `Object` (Class): Base game object type.
- `IterOrderType` (Enum): Iteration order modes (fastest, near/far, cheap/expensive).
- `ObjectIterator` (Class): Abstract iterator interface.
- `SimpleObjectIterator` (Class): Concrete iterator with sorting.
- `Clump` (Class): Internal node for sorted iteration.
- `ClumpCompareProc` (Class): Comparison function type for sorting.

## Key Functions
### `ObjectIterator::first()`
- Purpose: Reset iterator and return first object.
- Calls: None (pure virtual).

### `ObjectIterator::next()`
- Purpose: Advance and return next object.
- Calls: None (pure virtual).

### `SimpleObjectIterator::insert()`
- Purpose: Add object to iterator with optional numeric value.
- Calls: None.

### `SimpleObjectIterator::sort()`
- Purpose: Sort objects based on `IterOrderType`.
- Calls: `theClumpCompareProcs[order]`.

### `SimpleObjectIterator::nextWithNumeric()`
- Purpose: Get next object and optional numeric value.
- Calls: None.

## Globals
- `theClumpCompareProcs` (ClumpCompareProc[]): Array of sorting comparison functions.

## Dependencies
- `Common/GameType.h`, `Common/GameMemory.h`
- `MemoryPoolObject`, `Real`, `Int`
