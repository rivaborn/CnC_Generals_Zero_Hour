# Generals/Code/Tools/Babylon/list.h

## Purpose
Provides a doubly-linked list implementation with priority support and search utilities.

## Responsibilities
- Manages list nodes and their priorities
- Supports insertion, removal, and traversal
- Provides search functionality via ListSearch
- Handles list merging and emptying

## Key Types
- **ListNode (Class)**: Represents a node in the list with priority and item storage
- **List (Class)**: Manages the list structure and operations
- **ListSearch (Class)**: Facilitates list traversal and searching

## Key Functions
### ListNode::Link
- Purpose: Links this node to another node
- Calls: Not inferable

### List::AddToTail
- Purpose: Adds a node to the end of the list
- Calls: Not inferable

### List::Merge
- Purpose: Merges another list into this one
- Calls: Not inferable

### ListSearch::Next
- Purpose: Advances the search to the next node
- Calls: ListNode::Next

## Globals
- **LOWEST_PRIORITY (int)**: Lowest possible priority value
- **HIGHEST_PRIORITY (int)**: Highest possible priority value
- **NORMAL_PRIORITY (int)**: Default priority value

## Dependencies
- No external includes or dependencies visible in this header file
