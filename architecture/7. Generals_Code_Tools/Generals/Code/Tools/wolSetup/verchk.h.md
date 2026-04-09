# Generals/Code/Tools/wolSetup/verchk.h

## Purpose
Header file for version checking utilities in the WOL setup tool.

## Responsibilities
- Declares version info retrieval functions
- Provides Windows API compatibility macros
- Exposes WOL API loading function

## Key Types
None

## Key Functions
### GetVersionInfo
- Purpose: Retrieves version info from a file
- Calls: Not inferable

### loadWolapi
- Purpose: Loads the WOL API from a specified file
- Calls: Not inferable

## Globals
None

## Dependencies
- `<windows.h>` (via WIN32_LEAN_AND_MEAN)
- `VS_FIXEDFILEINFO` (Windows version info structure)
