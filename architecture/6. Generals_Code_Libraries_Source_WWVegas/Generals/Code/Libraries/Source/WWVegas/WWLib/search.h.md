# Generals/Code/Libraries/Source/WWVegas/WWLib/search.h

## Purpose
Provides a template-based index management system for efficient lookup of data elements by integer IDs.

## Responsibilities
- Manages a dynamic array of indexed data elements
- Supports fast lookup via binary search
- Handles dynamic resizing of internal storage
- Mainages an archive pointer for caching recently accessed elements

## Key Types
- **IndexClass<T> (Class)**: Template class for managing indexed data elements
- **NodeElement (Struct)**: Internal structure pairing an ID with associated data

## Key Functions
### IndexClass<T>::Add_Index
- Purpose: Adds a new indexed element to the collection
- Calls: Increase_Table_Size

### IndexClass<T>::Remove_Index
- Purpose: Removes an element by its ID
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
- bool.h
- W3DNEWARRAY (memory allocation)
- qsort, bsearch (standard library functions)
