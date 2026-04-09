# GeneralsMD/Code/GameEngine/Source/Common/System/List.cpp

## Purpose
Implements a doubly-linked list data structure with priority-based sorting and node management.

## Responsibilities
- Manages list nodes and their insertion/removal
- Supports priority-based sorting (ascending/descending)
- Provides iteration and search functionality
- Handles memory management for nodes

## Key Types
- LList (Class): Main list container with sorting capabilities
- LListNode (Class): Individual list node storing data and priority
- LListSortMode (Enum): Defines sorting order (ASCENDING/DESCENDING)

## Key Functions
### LList::add
- Purpose: Inserts a node into the list at the correct priority position
- Calls: LListNode::priority(), LListNode::append(), LListNode::insert()

### LList::clear
- Purpose: Removes and destroys all nodes in the list
- Calls: LListNode::remove(), LListNode::destroy()

### LList::findItem
- Purpose: Searches for a node containing a specific item pointer
- Calls: LListNode::item(), LListNode::next()

### LListNode::insert
- Purpose: Inserts a new node before the current node
- Calls: None

### LListNode::destroy
- Purpose: Deletes the node if auto-delete is enabled
- Calls: None

## Globals
- None

## Dependencies
- "Common/List.h" (header)
- NEW operator (memory allocation)
- delete operator (memory deallocation)
