# Generals/Code/Tools/Autorun/WSYS_RAMFile.h

## Purpose
Defines the RAMFile class, a memory-based file abstraction for fast read/write operations.

## Responsibilities
- Provides in-memory file operations (open, close, read, write, seek)
- Manages memory buffer for file data
- Implements File interface for RAM-based access

## Key Types
- **RAMFile (Class)**: Memory-based file abstraction with standard file operations.

## Key Functions
### RAMFile::open(const Char *filename, Int access)
- Purpose: Opens a file for access.
- Calls: Not inferable.

### RAMFile::open(File *file)
- Purpose: Opens a file for fast RAM access.
- Calls: Not inferable.

### RAMFile::close()
- Purpose: Closes the file.
- Calls: Not inferable.

### RAMFile::read(void *buffer, Int bytes)
- Purpose: Reads bytes into buffer.
- Calls: Not inferable.

### RAMFile::write(void *buffer, Int bytes)
- Purpose: Writes bytes from buffer.
- Calls: Not inferable.

### RAMFile::seek(Int new_pos, seekMode mode)
- Purpose: Sets file position.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- **wsys_File.h**: Base File class interface.
