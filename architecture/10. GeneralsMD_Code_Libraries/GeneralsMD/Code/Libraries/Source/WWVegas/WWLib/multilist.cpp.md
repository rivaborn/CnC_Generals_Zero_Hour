# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/multilist.cpp

## Purpose
Implements a multi-list data structure allowing objects to belong to multiple lists simultaneously.

## Responsibilities
- Manages list nodes for objects in multiple lists
- Provides insertion/removal operations (head, tail, after existing member)
- Tracks object membership across lists
- Handles memory allocation/deallocation for list nodes

## Key Types
- `MultiListObjectClass`: base class for objects that can be in multiple lists
- `GenericMultiListClass`: core implementation handling void* objects
- `MultiListNodeClass`: internal node structure linking objects to lists

## Key Functions
### `~GenericMultiListClass()`
- Purpose: Destructor ensuring list is empty before deletion
- Calls: `assert(Is_Empty())`

### `Internal_Add()`
- Purpose: Adds object to list, optionally preventing duplicates
- Calls: `new MultiListNodeClass`, `WWMEMLOG`

### `Internal_Remove()`
- Purpose: Removes object from specific list
- Calls: `delete` on node, updates object's list node chain

### `Internal_Remove_List_Head()`
- Purpose: Removes and returns first object in list
- Calls: `Internal_Remove()`

## Globals
- `MultiListNodeClass` pool (256 elements): memory management for list nodes

## Dependencies
- `multilist.h`: header with class declarations
- `wwmemlog.h`: memory logging utilities
- `assert.h`: for debugging checks
