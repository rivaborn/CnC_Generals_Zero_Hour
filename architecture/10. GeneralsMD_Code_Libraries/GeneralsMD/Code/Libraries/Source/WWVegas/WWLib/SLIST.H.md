# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/SLIST.H

## Purpose
Header file defining a singly-linked list template class (SList) for managing node-based data structures.

## Responsibilities
- Provides core operations for singly-linked list manipulation
- Manages node insertion/removal at head/tail
- Supports list traversal and element searching
- Handles memory cleanup for list nodes

## Key Types
- SList<T> (Class): Template class for singly-linked list management
- SLNode<T> (Class): Node structure (defined in slnode.h)

## Key Functions
### Insert_Before
- Purpose: Inserts a node before a specified node or at head if null
- Calls: Add_Head

### Insert_After
- Purpose: Inserts a node after a specified node or at head if null
- Calls: Add_Head, Add_Tail

### Remove_All
- Purpose: Deletes all nodes in the list
- Calls: None (direct memory operations)

### Remove
- Purpose: Removes a specific element from the list
- Calls: Remove_Head

### Remove_Head
- Purpose: Removes and returns the head node's data
- Calls: None

### Remove_Tail
- Purpose: Removes and returns the tail node's data
- Calls: Remove

### Add_Head
- Purpose: Adds data to the head of the list (two overloads)
- Calls: None

### Add_Tail
- Purpose: Adds data to the tail of the list (two overloads)
- Calls: None

### Find_Node
- Purpose: Finds first node containing specified data
- Calls: None

## Globals
- None

## Dependencies
- slnode.h (for SLNode<T> class)
- NULL macro definition
