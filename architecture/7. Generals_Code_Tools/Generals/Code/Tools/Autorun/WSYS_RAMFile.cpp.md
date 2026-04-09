# Generals/Code/Tools/Autorun/WSYS_RAMFile.cpp

## Purpose
Implements a RAM-based file abstraction for the WSYS library, allowing file operations to be performed on data loaded entirely into memory.

## Responsibilities
- Load entire file contents into memory
- Provide standard file operations (read, seek) on in-memory data
- Manage memory allocation/deallocation for file data
- Interface with the WSYS file system

## Key Types
- **RAMFile (Class)**: In-memory file implementation
- **seekMode (Enum)**: Seek position modes (START, CURRENT, END)

## Key Functions
### RAMFile::open
- Purpose: Opens a file and loads its contents into memory
- Calls: TheFileSystem->open(), File::open(), file->read()

### RAMFile::read
- Purpose: Reads data from the in-memory file buffer
- Calls: memcpy()

### RAMFile::seek
- Purpose: Changes the current read position within the in-memory file
- Calls: None

## Globals
- **TheFileSystem (External)**: Global file system interface

## Dependencies
- WSYS_FileSystem.h
- WSYS_RAMFile.h
- Standard C I/O headers (stdio.h, fcntl.h, etc.)
