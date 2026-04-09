# Generals/Code/Tools/WW3D/pluglib/rawfile.cpp

## Purpose
Implements a cross-platform file I/O abstraction class (RawFileClass) for the SAGE engine.

## Responsibilities
- File opening/closing with bias support
- Read/write operations with error handling
- File metadata (size, date/time) management
- Cross-platform compatibility (Windows/Unix)

## Key Types
- RawFileClass (Class): Cross-platform file I/O wrapper
- FILE_HANDLE (Type): Platform-specific file handle type

## Key Functions
### RawFileClass::Open
- Purpose: Opens a file with specified access rights
- Calls: Set_Name, Error, GetLastError

### RawFileClass::Read
- Purpose: Reads data from the file
- Calls: Error, GetLastError

### RawFileClass::Write
- Purpose: Writes data to the file
- Calls: Error, GetLastError

### RawFileClass::Size
- Purpose: Determines file size in bytes
- Calls: Error, GetLastError

### RawFileClass::Bias
- Purpose: Sets artificial start position and length for the file
- Calls: Size

## Globals
None

## Dependencies
- Key includes: "rawfile.h", "win.h", <stdio.h>, <stdlib.h>, <string.h>
- External symbols: GetLastError, DeleteFile, SetFilePointer, GetFileInformationByHandle, etc.
