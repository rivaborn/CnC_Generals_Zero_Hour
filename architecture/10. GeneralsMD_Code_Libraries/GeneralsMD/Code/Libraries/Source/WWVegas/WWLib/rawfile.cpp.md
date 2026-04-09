# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rawfile.cpp

## Purpose
Implements the `RawFileClass` for file I/O operations, handling file opening, reading, writing, seeking, and error management.

## Responsibilities
- File I/O operations (read/write/seek)
- File creation, deletion, and metadata handling
- Error reporting and recovery
- File biasing (virtual sub-files within a file)
- Cross-platform compatibility (Windows/Unix)

## Key Types
- `RawFileClass` (Class): Wraps file operations with biasing and error handling
- `NULL_HANDLE` (Type): Represents an invalid file handle

## Key Functions
### `Open`
- Purpose: Opens a file with specified access rights
- Calls: `Close`, `Error`, platform-specific file open functions

### `Read`
- Purpose: Reads data from the file into a buffer
- Calls: `Error`, platform-specific read functions

### `Write`
- Purpose: Writes data from a buffer to the file
- Calls: `Error`, platform-specific write functions

### `Seek`
- Purpose: Moves the file pointer to a specified position
- Calls: `Error`, `Raw_Seek`

### `Bias`
- Purpose: Sets a virtual sub-file range within the file
- Calls: `Size`, `Seek`

## Globals
None

## Dependencies
- Platform-specific headers (`stdio.h`, `win.h`, `unistd.h`)
- `StringClass` for filename storage
- Windows API (`GetFileInformationByHandle`, `SetFileTime`)
- Unix API (`stat`, `unlink`)
