# Generals/Code/GameEngine/Source/GameLogic/Object/SimpleObjectIterator.cpp

## Purpose
This file implements a simple object iterator for the Command & Conquer Generals game engine, allowing objects to be iterated and sorted based on various criteria.

## Responsibilities
- Manages a list of objects with associated numeric values.
- Provides methods to insert objects into the iterator.
- Supports sorting objects by different criteria (e.g., near to far, cheap to expensive).
- Iterates through the sorted list of objects.

## Key Types
- `SimpleObjectIterator::Clump`: A struct representing an element in the linked list of objects.
  - Purpose: Holds a reference to an object and its numeric value.

## Key Functions
### SimpleObjectIterator::insert
- Purpose: Inserts an object into the iterator with an associated numeric value.
- Calls:
  - `newInstance(Clump)()`
  - `deleteInstance()`

### SimpleObjectIterator::nextWithNumeric
- Purpose: Retrieves the next object in the iteration and its numeric value.
- Calls: None

### SimpleObjectIterator::reset
- Purpose: Resets the iterator to the beginning of the list.
- Calls: None

### SimpleObjectIterator::makeEmpty
- Purpose: Clears all objects from the iterator.
- Calls:
  - `deleteInstance()`

### SimpleObjectIterator::sort
- Purpose: Sorts the objects in the iterator based on a specified order type.
- Calls:
  - `sortNearToFar`
  - `sortFarToNear`
  - `sortCheapToExpensive`
  - `sortExpensiveToCheap`

## Globals
- `theClumpCompareProcs[]`: An array of function pointers for sorting criteria.

## Dependencies
- Key includes and external symbols used but not defined here:
  - `"PreRTS.h"`
  - `"GameLogic/ObjectIter.h"`
  - `"Common/ThingTemplate.h"`
  - `"GameLogic/Object.h"`
