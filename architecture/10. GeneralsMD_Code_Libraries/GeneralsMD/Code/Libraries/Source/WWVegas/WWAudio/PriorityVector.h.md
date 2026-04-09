# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/PriorityVector.h

## Purpose
Defines a template class `PriorityVectorClass` that extends `DynamicVectorClass` to manage objects with priority-based insertion and processing.

## Responsibilities
- Provides priority-based object insertion (high/low priority).
- Manages object processing order via `Process_Head`.
- Inherits core vector operations from `DynamicVectorClass`.

## Key Types
- **PriorityVectorClass (Class)**: A priority-aware dynamic vector that supports high/low-priority insertion and head processing.

## Key Functions
### `Process_Head`
- Purpose: Moves the head object to the end of the vector and returns it.
- Calls: None (directly manipulates `Vector` and `ActiveCount`).

### `Add_Low`
- Purpose: Adds an object to the end of the vector (low priority).
- Calls: `DynamicVectorClass<T>::Add`.

### `Add_High`
- Purpose: Adds an object to the front of the vector (high priority).
- Calls: `DynamicVectorClass<T>::Add_Head`.

## Globals
- None.

## Dependencies
- `Vector.H` (inherits from `DynamicVectorClass<T>`).
- Uses `DynamicVectorClass<T>` methods (`Add`, `Add_Head`).
