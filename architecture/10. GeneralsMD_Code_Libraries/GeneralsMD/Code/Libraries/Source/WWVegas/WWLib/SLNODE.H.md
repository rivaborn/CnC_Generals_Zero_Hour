# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/SLNODE.H

## Purpose
Defines a singly-linked list node class for generic data storage in the SAGE engine.

## Responsibilities
- Provides base `GenericSLNode` for memory pooling and node management
- Implements templated `SLNode<T>` for type-safe node access
- Enforces construction with valid data via private default constructors
- Supports friend relationship with `SList<T>` for list management

## Key Types
- `GenericSLNode` (Class): Base node class with memory pooling and raw pointer access
- `SLNode<T>` (Template Class): Typed wrapper for `GenericSLNode` with `T*` data access

## Key Functions
### `GenericSLNode::Internal_Get_Next`
- Purpose: Retrieves the next node pointer
- Calls: None

### `GenericSLNode::Internal_Set_Next`
- Purpose: Sets the next node pointer
- Calls: None

### `SLNode<T>::Next`
- Purpose: Returns the next node in the list
- Calls: `Internal_Get_Next`

### `SLNode<T>::Data`
- Purpose: Returns the data payload of the node
- Calls: `Internal_Get_Data`

## Globals
- None

## Dependencies
- `always.h`: Header for common macros
- `mempool.h`: Memory pooling infrastructure
- `AutoPoolClass`: Base class for memory-pooled objects
