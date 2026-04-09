# Generals/Code/Tools/WW3D/max2w3d/dllmain.h

## Purpose
Header file defining core DLL entry points and string retrieval for the max2w3d tool.

## Responsibilities
- Declares global application instance handle
- Defines string retrieval function
- Sets constant string length limits
- Provides Windows API compatibility macros

## Key Types
None

## Key Functions
### Get_String
- Purpose: Retrieves a localized string by ID
- Calls: Not inferable

## Globals
- AppInstance (HINSTANCE): Stores the DLL instance handle

## Dependencies
- `<windows.h>` for Windows API types
- `_MAX_PATH` from Windows SDK
- `TCHAR` type for Unicode/ANSI compatibility
