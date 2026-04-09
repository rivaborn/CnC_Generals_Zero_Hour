# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/LISTNODE.H

## Purpose
Provides a generic doubly-linked list implementation for the SAGE engine, supporting node management and data association.

## Responsibilities
- Defines `GenericNode` and `GenericList` for basic linked list operations
- Provides templated `Node` and `List` classes for type-safe list management
- Implements specialized node types (`DataNode`, `ContextDataNode`, etc.) for data association
- Supports double-linked nodes (`DoubleNode`) for objects in multiple lists

## Key Types
- **GenericNode (class)**: Base class for doubly-linked list nodes
- **GenericList (class)**: Container managing a list of `GenericNode` objects
- **Node<T> (template class)**: Type-safe wrapper for `GenericNode`
- **List<T> (template class)**: Type-safe wrapper for `GenericList`
- **DataNode<T> (template class)**: Node with associated data of type T
- **ContextDataNode<C,D> (template class)**: Extends `DataNode` with context data
- **SafeContextDataNode<C,D> (template class)**: Enforces initialization of context/data
- **DoubleNode<P,S> (template class)**: Node with two data values for dual-list membership

## Key Functions
### `GenericNode::Unlink()`
- Purpose: Removes the node from its list
- Calls: None

### `GenericList::Add_Head()`
- Purpose: Adds a node to the beginning of the list
- Calls: `GenericNode::Link()`

### `List<T>::Delete()`
- Purpose: Deletes all nodes in the list
- Calls: `GenericNode::Is_Valid()`, `operator delete`

## Globals
None

## Dependencies
- `assert.h` for debugging checks
- Uses `operator new`/`delete` for memory management
