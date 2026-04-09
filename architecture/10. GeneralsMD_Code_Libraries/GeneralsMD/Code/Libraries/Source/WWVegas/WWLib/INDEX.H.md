# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/INDEX.H

## Purpose
This file defines a template-based index management system for mapping unique identifiers to data objects.

## Responsibilities
- Provides a container class for mapping identifiers to data objects
- Manages dynamic resizing of internal storage
- Supports fast lookup via binary search
- Handles caching of recently accessed entries for performance

## Key Types
- **IndexClass<INDEX, T> (class)**: Main template class for index management
- **NodeElement (struct)**: Internal structure linking IDs to data objects
- **search_compfunc (function)**: Comparison function for binary search operations

## Key Functions
### IndexClass::Add_Index
- Purpose: Adds a new index entry with associated data
- Calls: Increase_Table_Size

### IndexClass::Remove_Index
- Purpose: Removes an index entry by ID
- Calls: None

### IndexClass::Is_Present
- Purpose: Checks if an index exists
- Calls: Is_Archive_Same, Search_For_Node

### IndexClass::Search_For_Node
- Purpose: Performs binary search for an index
- Calls: qsort, Binary_Search

### IndexClass::operator[]
- Purpose: Retrieves data by index ID
- Calls: Is_Present

## Globals
- None

## Dependencies
- bsearch.h (for Binary_Search and qsort)
- W3DNEWARRAY (memory allocation)
- assert (for debugging checks)
