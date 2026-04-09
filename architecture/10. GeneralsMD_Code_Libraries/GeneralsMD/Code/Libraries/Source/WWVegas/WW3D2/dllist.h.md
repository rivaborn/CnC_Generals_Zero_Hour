# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dllist.h

## Purpose
Provides a doubly-linked list implementation with node management for the SAGE engine.

## Responsibilities
- Defines `DLListClass` for list operations (add/remove head/tail).
- Defines `DLNodeClass` for node operations (insert/remove, successor/predecessor).
- Provides `DLDestroyListClass` for automatic node deletion on list destruction.
- Manages list head/tail pointers and node links.

## Key Types
- **DLListClass (Class)**: Doubly-linked list container.
- **DLNodeClass (Class)**: Node within a doubly-linked list.
- **DLDestroyListClass (Class)**: List that auto-deletes nodes on destruction.

## Key Functions
### `DLListClass<T>::Add_Head`
- Purpose: Adds a node to the head of the list.
- Calls: `DLNodeClass<T>::Insert_Before`, `DLNodeClass<T>::Remove`.

### `DLListClass<T>::Add_Tail`
- Purpose: Adds a node to the tail of the list.
- Calls: `DLNodeClass<T>::Insert_After`.

### `DLListClass<T>::Remove_Head`
- Purpose: Removes the head node from the list.
- Calls: `DLNodeClass<T>::Remove`.

### `DLListClass<T>::Remove_Tail`
- Purpose: Removes the tail node from the list.
- Calls: `DLNodeClass<T>::Remove`.

### `DLNodeClass<T>::Insert_Before`
- Purpose: Inserts the node before another node.
- Calls: None.

### `DLNodeClass<T>::Insert_After`
- Purpose: Inserts the node after another node.
- Calls: None.

### `DLNodeClass<T>::Remove`
- Purpose: Removes the node from its list.
- Calls: `DLListClass<T>::Remove_Head`, `DLListClass<T>::Remove_Tail`.

## Globals
- None.

## Dependencies
- `W3DMPO` (base class for `DLNodeClass`).
- Standard C++ templates and operators.
