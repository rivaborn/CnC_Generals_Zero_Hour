# Generals/Code/Libraries/Source/WWVegas/WW3D2/dllist.h

## Purpose
This file defines a doubly-linked list implementation with node management for the SAGE engine.

## Responsibilities
- Provides `DLListClass` for managing a doubly-linked list.
- Defines `DLNodeClass` for list nodes with insertion/removal logic.
- Implements `DLDestroyListClass` for automatic node deletion on destruction.
- Supports head/tail insertion and removal operations.
- Manages node relationships (successor/predecessor).

## Key Types
- **DLListClass (Class)**: Manages a doubly-linked list of nodes.
- **DLNodeClass (Class)**: Represents a node in the list with insertion/removal methods.
- **DLDestroyListClass (Class)**: Extends `DLListClass` to auto-delete nodes on destruction.

## Key Functions
### `DLListClass<T>::Add_Head`
- Purpose: Adds a node to the head of the list.
- Calls: `n->Insert_Before`, `n->Remove`.

### `DLListClass<T>::Add_Tail`
- Purpose: Adds a node to the tail of the list.
- Calls: `n->Insert_After`, `n->Remove`.

### `DLListClass<T>::Remove_Head`
- Purpose: Removes the head node from the list.
- Calls: `n->Remove`.

### `DLListClass<T>::Remove_Tail`
- Purpose: Removes the tail node from the list.
- Calls: `n->Remove`.

### `DLNodeClass<T>::Insert_Before`
- Purpose: Inserts the node before another node in the list.
- Calls: None.

### `DLNodeClass<T>::Insert_After`
- Purpose: Inserts the node after another node in the list.
- Calls: None.

### `DLNodeClass<T>::Remove`
- Purpose: Removes the node from its list.
- Calls: `list->Remove_Head`, `list->Remove_Tail`.

## Globals
- None.

## Dependencies
- Key includes: None (header-only).
- External symbols: `W3DMPO` (base class for `DLNodeClass`).
