# Generals/Code/Libraries/Source/WWVegas/WWLib/verchk.h

## Purpose
Header file providing version checking utilities for Windows executables.

## Responsibilities
- Declares functions for retrieving version info and file creation time
- Provides executable version comparison functionality
- Exposes Windows API wrappers for version resource access

## Key Types
None

## Key Functions
### GetVersionInfo
- Purpose: Retrieves version information from a specified file
- Calls: Not inferable

### GetFileCreationTime
- Purpose: Retrieves the creation time of a specified file
- Calls: Not inferable

### Compare_EXE_Version
- Purpose: Compares versions between current process and a saved executable
- Calls: Not inferable

## Globals
None

## Dependencies
- `<windows.h>` for Windows API types
- `VS_FIXEDFILEINFO` and `FILETIME` structs from Windows API
