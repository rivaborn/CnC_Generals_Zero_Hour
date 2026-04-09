# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ntree.h

## Purpose
This file defines template classes for managing hierarchical tree structures with leaf nodes, supporting both unsorted and sorted insertion.

## Responsibilities
- Provides `NTreeClass` for basic tree management
- Implements `SortedNTreeClass` for alphabetically sorted trees
- Defines `NTreeLeafClass` and `SortedNTreeLeafClass` for node management
- Handles reference counting for tree nodes
- Supports insertion, removal, and traversal operations

## Key Types
- `NTreeClass<T>` (Class): Base tree container class
- `SortedNTreeClass<T>` (Class): Tree class with sorted insertion
- `NTreeLeafClass<T>` (Class): Basic tree node implementation
- `SortedNTreeLeafClass<T>` (Class): Tree node with sorting capabilities
- `StringClass` (Type): Used for node names in sorted trees

## Key Functions
### `NTreeClass<T>::Add`
- Purpose: Adds a value to the tree
- Calls: `Allocate_Leaf()`, `Set_Value()`, `Add()`

### `SortedNTreeClass<T>::Add_Sorted`
- Purpose: Adds a value to the tree in sorted order
- Calls: `Allocate_Leaf()`, `Set_Name()`, `Insertion_Sort()`

### `NTreeLeafClass<T>::Add_Child`
- Purpose: Adds a child node to the current node
- Calls: `W3DNEW`, `Set_Value()`, `Set_Parent()`

### `SortedNTreeLeafClass<T>::Insertion_Sort`
- Purpose: Inserts a node in sorted order by name
- Calls: `Get_Name()`, `Set_Prev()`, `Set_Next()`

## Globals
None

## Dependencies
- `refcount.h`: For reference counting functionality
- `wwstring.h`: For `StringClass` usage
- `W3DNEW`: Memory allocation macro
- `REF_PTR_SET/RELEASE`: Reference counting macros
- `stricmp`: String comparison function
