# Generals/Code/Libraries/Source/WWVegas/WWLib/multilist.cpp

## Purpose
Implements a multi-list data structure allowing objects to belong to multiple lists simultaneously.

## Responsibilities
- Manages list nodes for objects in multiple lists
- Provides core list operations (add/remove/iterate)
- Handles memory allocation for list nodes
- Supports both head and tail insertion
- Maintains bidirectional links between objects and lists

## Key Types
- `MultiListObjectClass`: base class for objects that can be in multiple lists
- `GenericMultiListClass`: core implementation handling void* objects
- `MultiListNodeClass`: internal node structure linking objects to lists

## Key Functions
### `~MultiListObjectClass()`
- Purpose: Cleans up all list nodes when object is destroyed
- Calls: `Internal_Remove`

### `Contains()`
- Purpose: Checks if an object is in this list
- Calls: `Get_List_Node()`

### `Internal_Add()`
- Purpose: Adds object to list (head insertion)
- Calls: `new MultiListNodeClass`, `Get_List_Node()`, `Set_List_Node()`

### `Internal_Remove()`
- Purpose: Removes object from this specific list
- Calls: `Get_List_Node()`, `Set_List_Node()`, `delete`

### `Internal_Remove_List_Head()`
- Purpose: Removes and returns first object in list
- Calls: `Internal_Remove()`

## Globals
- `MEM_GAMEDATA` (Type not shown): memory logging category
- Auto pool for `MultiListNodeClass` (256 elements)

## Dependencies
- `multilist.h` (header with templates)
- `wwmemlog.h` (memory logging)
- Uses `assert()` for debugging
- Relies on `WWMEMLOG` macro for memory tracking
