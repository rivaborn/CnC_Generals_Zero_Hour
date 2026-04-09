# Generals/Code/Tools/WW3D/pluglib/nodelist.h

## Purpose
Defines classes for enumerating and filtering 3dsMax scene nodes based on criteria.

## Responsibilities
- Provides `INodeListClass` to build and manage lists of filtered scene nodes
- Supports node insertion, removal, and sorting
- Enables tree traversal and node enumeration via callback
- Defines comparison interface for node sorting

## Key Types
- `INodeListEntryClass` (Class): Not inferable (forward declaration)
- `INodeCompareClass` (Class): Abstract base for node comparison logic
- `INodeListClass` (Class): Main class for node list management and filtering

## Key Functions
### `INodeListClass::Set_Filter`
- Purpose: Sets the node filter for the list
- Calls: None

### `INodeListClass::Insert`
- Purpose: Adds nodes or another list to the current list
- Calls: None (implementation not shown)

### `INodeListClass::Sort`
- Purpose: Sorts nodes using a provided comparison object
- Calls: None (implementation not shown)

### `INodeListClass::Add_Tree`
- Purpose: Recursively adds nodes from a tree structure
- Calls: None (implementation not shown)

### `INodeCompareClass::operator()`
- Purpose: Abstract comparison method for node ordering
- Calls: None

## Globals
- None

## Dependencies
- `always.h`, `<Max.h>`, `nodefilt.h`
- `INode`, `IScene`, `ITreeEnumProc` (3dsMax SDK types)
