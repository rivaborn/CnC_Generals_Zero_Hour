# Generals/Code/Tools/Babylon/list.cpp

## Purpose
Implements a doubly-linked list data structure with priority-based insertion and node management.

## Responsibilities
- Manages `ListNode` and `List` classes for linked list operations
- Supports priority-based insertion and merging of lists
- Provides iteration, searching, and item access methods
- Handles node insertion, removal, and traversal

## Key Types
- `ListNode` (Class): Represents a node in the list with priority and item storage
- `List` (Class): Manages the list head and provides high-level list operations
- `Priority` (Enum): Not inferable (used as integer values in assertions)

## Key Functions
### `ListNode::Append`
- Purpose: Adds a new node after the current node
- Calls: None

### `ListNode::Prepend`
- Purpose: Adds a new node before the current node
- Calls: None

### `ListNode::Remove`
- Purpose: Removes the node from its list
- Calls: None

### `List::Add`
- Purpose: Inserts a node into the list based on priority
- Calls: `ListNode::Priority`, `ListNode::Prepend`, `ListNode::Next`

### `List::Merge`
- Purpose: Merges another list into this one
- Calls: `ListNode::Link`, `List::Empty`

### `List::Find`
- Purpose: Searches for a node containing a specific item
- Calls: `ListNode::Item`, `ListNode::Next`

## Globals
- None

## Dependencies
- `<assert.h>` for debugging assertions
- `list.h` for class declarations
- Uses `stdAfx.h` (likely precompiled headers)
