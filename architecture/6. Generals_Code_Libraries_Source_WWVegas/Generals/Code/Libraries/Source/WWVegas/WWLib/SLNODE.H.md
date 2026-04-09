# Generals/Code/Libraries/Source/WWVegas/WWLib/SLNODE.H

## Purpose
Defines a singly-linked list node class for generic data storage in the SAGE engine.

## Responsibilities
- Provides base `GenericSLNode` for memory management via `AutoPoolClass`.
- Implements typed `SLNode<T>` for type-safe node access.
- Manages next-pointer and data-pointer links for list traversal.
- Restricts node creation to require valid data objects.

## Key Types
- `GenericSLNode` (Class): Base node class with protected internal accessors.
- `SLNode<T>` (Template Class): Typed wrapper for `GenericSLNode` with public accessors.

## Key Functions
### `Internal_Get_Next()`
- Purpose: Retrieves the next node pointer.
- Calls: None.

### `Internal_Set_Next(void* n)`
- Purpose: Sets the next node pointer.
- Calls: None.

### `Next()`
- Purpose: Returns the next node as `SLNode<T>`.
- Calls: `Internal_Get_Next()`.

### `Data()`
- Purpose: Returns the nodeâs data as type `T`.
- Calls: `Internal_Get_Data()`.

## Globals
- None.

## Dependencies
- `always.h`: Engine-wide macros.
- `mempool.h`: Memory allocation utilities (`AutoPoolClass`).
