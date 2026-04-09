# Generals/Code/GameEngine/Source/Common/System/RAMFile.cpp

## Purpose
This file implements the `RAMFile` class, which provides functionality for reading files into memory and accessing their contents through a file-like interface.

## Responsibilities
- Reading files into memory.
- Providing methods to read, seek, and close the in-memory file.
- Supporting operations like scanning integers, reals, and strings from the file data.

## Key Types
- `RAMFile` (Class): Manages file data loaded into RAM and provides file-like operations on it.

## Key Functions
### RAMFile::open
- Purpose: Opens a file and reads its contents into memory.
- Calls: 
  - `TheFileSystem->openFile`
  - `open(File*)`

### RAMFile::close
- Purpose: Closes the in-memory file and frees allocated memory.
- Calls: 
  - `delete[] m_data`
  - `File::close()`

### RAMFile::read
- Purpose: Reads a specified number of bytes from the current position in the file.
- Calls: 
  - `memcpy`

### RAMFile::seek
- Purpose: Moves the read/write pointer to a new position in the file.
- Calls: None

### RAMFile::scanInt
- Purpose: Scans and returns an integer from the file data at the current position.
- Calls: None

### RAMFile::scanReal
- Purpose: Scans and returns a real number (float) from the file data at the current position.
- Calls: None

### RAMFile::scanString
- Purpose: Scans and returns a string from the file data at the current position.
- Calls: None

## Globals
- None

## Dependencies
- `PreRTS.h`
- `<stdio.h>`
- `<fcntl.h>`
- `<io.h>`
- `<string.h>`
- `<sys/stat.h>`
- `"Common/AsciiString.h"`
- `"Common/FileSystem.h"`
- `"Common/RAMFile.h"`
- `"Common/PerfTimer.h"`
