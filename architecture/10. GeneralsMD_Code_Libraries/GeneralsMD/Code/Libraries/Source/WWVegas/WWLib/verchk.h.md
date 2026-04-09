# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/verchk.h

## Purpose
Header file declaring functions for version checking and file metadata retrieval on Windows.

## Responsibilities
- Declares version info retrieval functions
- Provides file creation time lookup
- Exposes EXE version comparison utility

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
- Purpose: Compares current process EXE version with a saved EXE version
- Calls: Not inferable

## Globals
None

## Dependencies
- `<windows.h>` for Windows API types
- `VS_FIXEDFILEINFO` (from Windows SDK)
- `FILETIME` (from Windows SDK)
