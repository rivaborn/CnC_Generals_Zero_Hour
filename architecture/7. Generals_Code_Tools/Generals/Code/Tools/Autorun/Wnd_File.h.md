# Generals/Code/Tools/Autorun/Wnd_File.h

## Purpose
Header file defining a cross-platform file I/O abstraction class (`StandardFileClass`) and related utilities.

## Responsibilities
- Declares `StandardFileClass` for file operations (open, read, write, seek, etc.).
- Provides file existence checks (`Full_Path_File_Exists`, `HD_File_Exists`, `CD_File_Exists`).
- Supports both stream-based and handle-based file I/O (configurable via macros).
- Includes debug messaging utilities (`Msg`).

## Key Types
- **StandardFileClass (Class)**: Wrapper for file operations with stream/handle backends.
- **None**: No enums/structs beyond standard C types.

## Key Functions
### StandardFileClass::Open
- Purpose: Opens a file with specified mode.
- Calls: Not inferable (implementation in `.cpp`).

### StandardFileClass::Read
- Purpose: Reads data from the open file.
- Calls: Not inferable.

### StandardFileClass::Write
- Purpose: Writes data to the open file.
- Calls: Not inferable.

### StandardFileClass::Seek
- Purpose: Moves file pointer to specified position.
- Calls: Not inferable.

### StandardFileClass::Query_Size
- Purpose: Returns the file size in bytes.
- Calls: Not inferable.

### Full_Path_File_Exists
- Purpose: Checks if a file exists at the given full path.
- Calls: Not inferable.

## Globals
- **SUPPORT_STREAMS (Macro)**: Enables/disables stream-based I/O.
- **SUPPORT_HANDLES (Macro)**: Enables/disables handle-based I/O.
- **MODE_READ_ONLY (Const)**: File open mode constant.
- **INVALID_FILE_HANDLE (Const)**: Invalid handle value.

## Dependencies
- `<stdio.h>`, `<sys/stat.h>`, `<sys/types.h>`, `<ctype.h>`, `<stdlib.h>`, `<assert.h>`
- `FILE`, `struct stat` (from C standard library)
- `HANDLE`, `INVALID_HANDLE_VALUE` (Windows-specific, if `SUPPORT_HANDLES` is true)
