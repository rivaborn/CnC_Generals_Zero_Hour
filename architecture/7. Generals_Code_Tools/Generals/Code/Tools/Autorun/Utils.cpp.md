# Generals/Code/Tools/Autorun/Utils.cpp

## Purpose
Utility functions for string manipulation, file operations, and path handling in the Autorun tool.

## Responsibilities
- String manipulation (ampersand handling, case conversion)
- File loading and memory allocation
- Path construction and modification
- Product name substitution in strings

## Key Types
None

## Key Functions
### Fix_Single_Ampersands
- Purpose: Replaces single '&' with '&&' in strings for dialog display
- Calls: lstrcpy, memset, toupper, strcpy (ANSI version); wcscpy, memset, toupper, wcscpy (Unicode version)

### Fix_Double_Ampersands
- Purpose: Replaces '&&' with single '&' in strings
- Calls: lstrcpy, memset, toupper, strcpy

### Load_Alloc_Data
- Purpose: Loads file contents into allocated memory buffer
- Calls: StandardFileClass::Open, Query_Open, Query_Size, malloc, memset, Read, Close, free

### Load_File
- Purpose: Wrapper for loading files from local directory
- Calls: Load_Alloc_Data

### Make_Current_Path_To
- Purpose: Constructs path relative to executable location
- Calls: Args->Get_argv, _splitpath, _makepath, Path_Add_Back_Slash, strcpy (ANSI); wcscpy, _wsplitpath, _wmakepath, Path_Add_Back_Slash, wcscpy (Unicode)

### Path_Add_Back_Slash
- Purpose: Ensures path ends with backslash
- Calls: strlen, strcat (ANSI); wcslen, wcscat (Unicode)

### Path_Remove_Back_Slash
- Purpose: Removes trailing backslash from path
- Calls: strlen (ANSI); wcslen (Unicode)

### PlugInProductName
- Purpose: Substitutes product names into formatted strings
- Calls: strcpy, strlen, strstr, sprintf (ANSI); wcscpy, wcslen, wcsstr, swprintf (Unicode)

## Globals
None

## Dependencies
- Key includes: io.h, args.h, assert.h, locale_api.h, resource.h, utils.h, winfix.h, wnd_file.h, winver.h, shlwapi.h
- External symbols: StandardFileClass, Args class, MAX_PATH, _MAX_PATH, _MAX_DRIVE, _MAX_DIR, MODE_READ_ONLY
