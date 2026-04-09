# Generals/Code/Tools/mangler/wlib/linkedlist.h

## Purpose
Implements a generic doubly-linked list template for storing copies of data nodes.

## Responsibilities
- Manages insertion/removal at any position
- Maintains a "current" pointer for sequential access
- Provides head/tail operations
- Handles list copying and clearing

## Key Types
- **LNode (Class)**: Node structure containing data, next/prev pointers
- **LinkedList (Class)**: Main list container with head/tail/current pointers

## Key Functions
### LinkedList::add
- Purpose: Inserts a node at specified position
- Calls: None (direct memory operations)

### LinkedList::remove
- Purpose: Removes node at specified position
- Calls: None (direct memory operations)

### LinkedList::getPointer
- Purpose: Retrieves pointer to node data without removal
- Calls: None (direct pointer operations)

### LinkedList::clear
- Purpose: Deletes all nodes and resets list state
- Calls: None (direct memory operations)

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<assert.h>`
- `wstypes.h` (for bit8/sint32 types)
- Uses `assert()` for debugging checks
