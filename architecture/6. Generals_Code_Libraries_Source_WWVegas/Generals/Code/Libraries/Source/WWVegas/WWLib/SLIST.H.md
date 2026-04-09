# Generals/Code/Libraries/Source/WWVegas/WWLib/SLIST.H

## Purpose
Implements a singly-linked list container class for managing collections of objects.

## Responsibilities
- Provides methods to add/remove nodes at head/tail
- Supports insertion before/after specific nodes
- Maintains list traversal capabilities
- Handles list concatenation and element removal
- Tracks list size and emptiness

## Key Types
- `SList<T>` (Class): Singly-linked list container template
- `SLNode<T>` (Class): Node structure (defined in slnode.h)

## Key Functions
### `Insert_Before`
- Purpose: Inserts a node before a specified node
- Calls: `Add_Head`, `SLNode<T>::Set_Next`

### `Insert_After`
- Purpose: Inserts a node after a specified node
- Calls: `Add_Head`, `Add_Tail`, `SLNode<T>::Set_Next`

### `Remove_All`
- Purpose: Removes all nodes from the list
- Calls: `delete` on each node

### `Remove`
- Purpose: Removes a specific element from the list
- Calls: `Remove_Head`, `SLNode<T>::Set_Next`

### `Remove_Head`
- Purpose: Removes and returns the head node's data
- Calls: `delete` on the head node

### `Remove_Tail`
- Purpose: Removes and returns the tail node's data
- Calls: `Remove`

### `Add_Head` (T*)
- Purpose: Adds a node to the head of the list
- Calls: `new SLNode<T>`, `SLNode<T>::Set_Next`

### `Add_Tail` (T*)
- Purpose: Adds a node to the tail of the list
- Calls: `new SLNode<T>`, `SLNode<T>::Set_Next`

### `Find_Node`
- Purpose: Finds the first node containing specified data
- Calls: `SLNode<T>::Data`, `SLNode<T>::Next`

## Globals
- `NULL` (macro): Defined as 0L if not already defined

## Dependencies
- `slnode.h` (include): Defines `SLNode<T>` class
- `new`/`delete` operators: For node allocation/deallocation
