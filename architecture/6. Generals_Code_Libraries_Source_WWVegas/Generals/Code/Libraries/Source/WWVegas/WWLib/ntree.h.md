# Generals/Code/Libraries/Source/WWVegas/WWLib/ntree.h

## Purpose
Defines template classes for managing hierarchical tree structures with leaf nodes, supporting both unsorted and sorted insertion.

## Responsibilities
- Provides base tree structure (`NTreeClass`) for generic hierarchical data
- Implements sorted tree variant (`SortedNTreeClass`) for ordered insertion
- Manages leaf nodes (`NTreeLeafClass`) with parent/child/sibling relationships
- Handles reference counting for memory management

## Key Types
- **NTreeClass (Class)**: Base tree container managing root node and leaf allocation
- **SortedNTreeClass (Class)**: Sorted tree variant extending `NTreeClass` with ordered insertion
- **NTreeLeafClass (Class)**: Tree node containing data and pointers to parent/child/siblings
- **SortedNTreeLeafClass (Class)**: Sorted node variant with name-based ordering and insertion

## Key Functions
### NTreeClass<T>::Add
- Purpose: Adds a value to the tree, creating root if empty
- Calls: `Allocate_Leaf()`, `Set_Value()`, `NTreeLeafClass<T>::Add()`

### NTreeLeafClass<T>::Add
- Purpose: Adds a sibling node to the current node
- Calls: `W3DNEW`, `Set_Value()`, `Set_Prev()`, `Set_Next()`

### SortedNTreeLeafClass<T>::Add_Sorted
- Purpose: Inserts a named value in sorted order among siblings
- Calls: `W3DNEW`, `Set_Value()`, `Set_Name()`, `Insertion_Sort()`

### SortedNTreeLeafClass<T>::Insertion_Sort
- Purpose: Performs insertion sort on sibling nodes by name
- Calls: `stricmp()`, `Set_Prev()`, `Set_Next()`

## Globals
- None

## Dependencies
- `refcount.h`: Reference counting utilities
- `wwstring.h`: String class for node names
- `W3DNEW`: Memory allocation macro
- `REF_PTR_SET/RELEASE`: Reference pointer management macros
