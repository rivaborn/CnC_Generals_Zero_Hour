# GeneralsMD/Code/GameEngine/Include/Common/List.h

## Purpose
Provides a linked list implementation (LList) and node structure (LListNode) for the game engine.

## Responsibilities
- Manages doubly-linked list operations (add/remove/iterate)
- Supports priority-based sorting (ascending/descending)
- Handles item storage and auto-deletion
- Provides list traversal and utility methods

## Key Types
- **LListNode (Class)**: Represents a node in the linked list, storing next/prev pointers, priority, and an item pointer
- **LList (Class)**: Manages the linked list, including sorting and node management
- **SortMode (Enum)**: Defines sorting order (ASCENDING/DESCENDING)

## Key Functions
### LListNode::remove
- Purpose: Removes the node from its containing list
- Calls: None

### LListNode::insert
- Purpose: Inserts a new node before this node
- Calls: None

### LList::add
- Purpose: Adds a node to the list sorted by priority
- Calls: None

### LList::addItem
- Purpose: Creates a node and adds an item to the list with specified priority
- Calls: None

### LList::clear
- Purpose: Deletes all items in the list
- Calls: None

## Globals
None

## Dependencies
- `<lib/BaseType.h>` (for Int, Bool, etc.)
- No external symbols used
