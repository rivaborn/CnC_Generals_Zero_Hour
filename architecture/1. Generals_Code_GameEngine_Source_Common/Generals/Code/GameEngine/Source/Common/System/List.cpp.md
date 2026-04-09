# Generals/Code/GameEngine/Source/Common/System/List.cpp

## Purpose
This file implements a doubly linked list (`LList`) and its nodes (`LListNode`). The list supports adding, removing, and searching for items based on priority or reference.

## Responsibilities
- Manage a doubly linked list with head node.
- Add nodes to the list in sorted order based on priority.
- Remove nodes from the list.
- Search for nodes by item reference.
- Merge two lists.
- Count nodes in the list.
- Clear all nodes from the list.

## Key Types
- `LList` (Class): Manages a doubly linked list with head node.
- `LListNode` (Class): Represents a node in the doubly linked list.

## Key Functions
### LList::add
- Purpose: Adds a new node to the list in sorted order based on priority.
- Calls: `LListNode::append`, `LListNode::insert`

### LList::addItem
- Purpose: Creates a new node with an item and adds it to the list.
- Calls: `LListNode::setPriority`, `LListNode::setItem`, `LListNode::autoDelete`, `LList::add`

### LList::clear
- Purpose: Removes all nodes from the list and destroys them.
- Calls: `LListNode::remove`, `LListNode::destroy`

### LList::nodeCount
- Purpose: Returns the number of nodes in the list.
- Calls: None

### LList::getNode
- Purpose: Retrieves a node by its index.
- Calls: None

### LList::merge
- Purpose: Merges another list into this list.
- Calls: None

### LListNode::insert
- Purpose: Inserts a new node before the current node.
- Calls: None

### LListNode::append
- Purpose: Appends a new node after the current node.
- Calls: None

### LListNode::remove
- Purpose: Removes the current node from the list.
- Calls: None

## Globals
- `None`

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/List.h"
