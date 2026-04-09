# Generals/Code/Tools/Autorun/Utils.h

## Purpose
Header file providing utility functions for string manipulation, file operations, and path handling.

## Responsibilities
- String manipulation (ampersand handling, swapping)
- File loading and allocation
- Path manipulation (backslash handling)
- Product name plug-in functionality

## Key Types
- None

## Key Functions
### swap
- Purpose: Swaps two objects of the same type.
- Calls: None

### Fix_Single_Ampersands
- Purpose: Fixes single ampersands in strings.
- Calls: None

### Fix_Double_Ampersands
- Purpose: Fixes double ampersands in strings.
- Calls: None

### Load_Alloc_Data
- Purpose: Loads and allocates data from a file.
- Calls: None

### Load_File
- Purpose: Loads a file into memory.
- Calls: None

### Make_Current_Path_To
- Purpose: Makes a current path to a file.
- Calls: None

### Path_Add_Back_Slash
- Purpose: Adds a backslash to a path.
- Calls: None

### Path_Remove_Back_Slash
- Purpose: Removes a backslash from a path.
- Calls: None

### PlugInProductName
- Purpose: Plugs in a product name into a string.
- Calls: None

## Globals
- None

## Dependencies
- `<windows.h>` for Windows API types
- `LPSTR`, `wchar_t` from Windows API
