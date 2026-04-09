# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bfiofile.cpp

## Purpose
Implements a buffered file I/O class for efficient file operations with caching capabilities.

## Responsibilities
- Manages file caching and buffering
- Handles file read/write operations with buffering
- Provides file position management (seek)
- Supports file size queries
- Manages file opening/closing with buffering state

## Key Types
- `BufferIOFileClass` (Class): Buffered file I/O wrapper with caching
- `MINIMUM_BUFFER_SIZE` (const): Minimum buffer size constant

## Key Functions
### `Cache`
- Purpose: Loads part or all of a file into memory buffer
- Calls: `Is_Available`, `Size`, `Open`, `Seek`, `Read`, `Error`

### `Commit`
- Purpose: Writes buffered changes to disk
- Calls: `BASECLASS::Seek`, `BASECLASS::Write`, `BASECLASS::Close`

### `Write`
- Purpose: Writes data to file with buffering
- Calls: `Open`, `BASECLASS::Seek`, `BASECLASS::Write`, `BASECLASS::Read`, `Commit`, `Error`

### `Read`
- Purpose: Reads data from file with buffering
- Calls: `Open`, `BASECLASS::Seek`, `BASECLASS::Read`, `Commit`, `Error`

### `Seek`
- Purpose: Moves file pointer with buffering awareness
- Calls: `BASECLASS::Seek`, `Commit`

### `Close`
- Purpose: Closes file with buffered changes commit
- Calls: `Commit`, `BASECLASS::Close`

## Globals
- `MINIMUM_BUFFER_SIZE` (const int): Minimum buffer size constant

## Dependencies
- `bfiofile.h` (header)
- `always.h` (header)
- `string.h` (header)
- `BASECLASS` (inherited class)
- `Error()` (error handling function)
