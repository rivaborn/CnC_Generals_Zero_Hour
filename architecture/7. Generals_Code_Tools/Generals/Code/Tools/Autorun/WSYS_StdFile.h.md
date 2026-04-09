# Generals/Code/Tools/Autorun/WSYS_StdFile.h

## Purpose
Header file defining the `StdFile` class, a file abstraction for standard C file operations.

## Responsibilities
- Declares `StdFile` class inheriting from `File`
- Provides virtual methods for file I/O (open, close, read, write, seek)
- Encapsulates a standard C file handle

## Key Types
- **StdFile (Class)**: File abstraction for standard C file operations.

## Key Functions
### StdFile::open
- Purpose: Opens a file for specified access mode.
- Calls: Not inferable.

### StdFile::close
- Purpose: Closes the file.
- Calls: Not inferable.

### StdFile::read
- Purpose: Reads bytes into a buffer.
- Calls: Not inferable.

### StdFile::write
- Purpose: Writes bytes from a buffer.
- Calls: Not inferable.

### StdFile::seek
- Purpose: Sets file position.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `wsys_File.h` (included)
- `File` (base class, not defined here)
