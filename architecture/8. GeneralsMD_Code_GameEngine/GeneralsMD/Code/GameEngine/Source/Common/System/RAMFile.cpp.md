# GeneralsMD/Code/GameEngine/Source/Common/System/RAMFile.cpp

## Purpose
Implements a RAM-based file abstraction for in-memory file operations in the SAGE engine.

## Responsibilities
- Loads entire files into memory for fast access
- Provides read/write operations on in-memory data
- Supports seeking, scanning, and parsing operations
- Handles file opening from archives and regular files
- Manages memory allocation/deallocation for file data

## Key Types
- RAMFile (Class): In-memory file implementation with read/write operations
- seekMode (Enum): Defines seek modes (START, CURRENT, END)

## Key Functions
### RAMFile::open
- Purpose: Opens a file and loads its contents into memory
- Calls: TheFileSystem->openFile, File::open, File::read

### RAMFile::read
- Purpose: Reads data from the in-memory file buffer
- Calls: memcpy

### RAMFile::seek
- Purpose: Changes the current read position within the file
- Calls: None

### RAMFile::scanInt
- Purpose: Parses an integer value from the current position
- Calls: atoi

### RAMFile::scanReal
- Purpose: Parses a floating-point value from the current position
- Calls: atof

### RAMFile::nextLine
- Purpose: Reads a line of text into a buffer
- Calls: None

## Globals
- None

## Dependencies
- Common/AsciiString.h
- Common/FileSystem.h
- Common/RAMFile.h
- Common/PerfTimer.h
- Standard C library headers (stdio.h, fcntl.h, etc.)
