# Generals/Code/Libraries/Source/WWVegas/WWLib/LISTNODE.H

## Purpose
Provides a generic doubly-linked list implementation for the game engine.

## Responsibilities
- Defines `GenericNode` and `GenericList` base classes for linked list operations
- Implements templated `Node` and `List` wrapper classes for type-safe usage
- Supports specialized node types (`DataNode`, `ContextDataNode`, etc.) for common patterns
- Manages list traversal, insertion, and deletion operations

## Key Types
- **GenericNode (class)**: Base node for doubly-linked lists
- **GenericList (class)**: Base list manager for `GenericNode` objects
- **Node<T> (template class)**: Type-safe wrapper for `GenericNode`
- **List<T> (template class)**: Type-safe wrapper for `GenericList`
- **DataNode<T> (template class)**: Node with associated data value
- **ContextDataNode<C,D> (template class)**: Node with context and data
- **SafeContextDataNode<C,D> (template class)**: ContextDataNode requiring constructor args
- **DoubleNode<P,S> (template class)**: Node belonging to two lists simultaneously

## Key Functions
### `GenericNode::Link`
- Purpose: Inserts a node into the list after the current node
- Calls: `Unlink`

### `GenericList::Add_Head`
- Purpose: Adds a node to the front of the list
- Calls: `FirstNode.Link`

### `GenericList::Add_Tail`
- Purpose: Adds a node to the end of the list
- Calls: `LastNode.Prev()->Link`

### `GenericList::Delete`
- Purpose: Deletes all nodes in the list
- Calls: `First()`, `Is_Valid()`, `delete`

## Globals
None

## Dependencies
- `assert.h` (for assertions)
- Uses `new`/`delete` operators for memory management
