# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_List.cpp

## Purpose
Implements a doubly-linked list data structure with priority-based sorting and iteration capabilities.

## Responsibilities
- Manages list initialization and node operations
- Supports priority-based insertion and merging
- Provides iteration and counting functions
- Handles node removal and traversal

## Key Types
- ListHead (struct): Head node of the list
- ListNode (struct): Node in the list with priority
- Priority (typedef): Priority value for sorting

## Key Functions
### ListInit
- Purpose: Initializes a list head node
- Calls: None

### ListAddNodeSortAscending
- Purpose: Inserts a node in ascending priority order
- Calls: ListNodeNext, ListNodeInsert

### ListMerge
- Purpose: Merges two lists
- Calls: None

### ListCountItems
- Purpose: Counts items in the list
- Calls: None

### ListNodeNext
- Purpose: Gets next node, skipping head
- Calls: ListNodeIsHead

### ListNodeLoopNext
- Purpose: Gets next node with head wrapping
- Calls: ListNodeIsHead

## Globals
None

## Dependencies
- wpaudio/altypes.h
- wpaudio/list.h
- ListNodeIsHead (external function)
