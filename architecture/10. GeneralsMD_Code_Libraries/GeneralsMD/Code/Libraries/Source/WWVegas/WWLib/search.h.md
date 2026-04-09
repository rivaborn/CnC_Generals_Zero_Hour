# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/search.h

## Purpose
Provides a template-based index management system using binary search for efficient lookups.

## Responsibilities
- Manages indexed data storage with unique integer IDs
- Supports adding, removing, and searching indexed elements
- Maintains sorted order for binary search operations
- Provides archive caching for recently accessed elements

## Key Types
- **IndexClass<T> (Class)**: Template class for managing indexed data
- **NodeElement (Struct)**: Internal structure pairing ID with data element

## Key Functions
### IndexClass<T>::Add_Index
- Purpose: Adds a new indexed element
- Calls: Increase_Table_Size

### IndexClass<T>::Remove_Index
- Purpose: Removes an indexed element by ID
- Calls: None

### IndexClass<T>::Is_Present
- Purpose: Checks if an ID exists in the index
- Calls: Is_Archive_Same, Search_For_Node, Set_Archive

### IndexClass<T>::Fetch_Index
- Purpose: Retrieves data associated with an ID
- Calls: Is_Present

### IndexClass<T>::Search_For_Node
- Purpose: Performs binary search for an ID
- Calls: qsort, bsearch, Invalidate_Archive

## Globals
- None

## Dependencies
- "bool.h" for boolean type
- qsort, bsearch (C standard library)
- W3DNEWARRAY (memory allocation)
- __BORLANDC__ (compiler-specific handling)
