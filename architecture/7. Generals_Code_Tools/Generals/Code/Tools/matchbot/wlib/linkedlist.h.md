# Generals/Code/Tools/matchbot/wlib/linkedlist.h

## Purpose
Provides a templated doubly-linked list implementation for the matchbot tool.

## Responsibilities
- Manages insertion/removal at any position
- Maintains a current pointer for sequential access
- Stores copies of data (not pointers)
- Supports list traversal and modification

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
- Purpose: Removes all entries and frees memory
- Calls: None (direct memory operations)

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<assert.h>`
- `wstypes.h` (for bit8/sint32 types)
- Uses `assert()` for debugging checks
