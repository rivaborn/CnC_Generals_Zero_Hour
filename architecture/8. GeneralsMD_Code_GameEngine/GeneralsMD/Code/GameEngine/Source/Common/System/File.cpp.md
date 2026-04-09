# GeneralsMD/Code/GameEngine/Source/Common/System/File.cpp

## Purpose
Base file I/O abstraction class for the SAGE engine, providing core file operations.

## Responsibilities
- Manages file open/close state
- Provides basic file operations (seek, size, position)
- Handles text/binary access modes
- Supports formatted text output
- Tracks file deletion on close

## Key Types
- File (Class): Base file abstraction with common operations
- AccessFlags (Enum): File access mode flags (READ, WRITE, etc.)

## Key Functions
### File::open
- Purpose: Initializes file handle and validates access flags
- Calls: setName

### File::close
- Purpose: Releases file resources and handles self-deletion if flagged
- Calls: setName, deleteInstance

### File::size
- Purpose: Determines file size via seek operations
- Calls: seek

### File::print
- Purpose: Formats and writes text data to file
- Calls: write, vsprintf

## Globals
None

## Dependencies
- Common/File.h (header)
- C standard library headers (assert.h, string.h, stdarg.h, stdio.h)
- PreRTS.h (engine precompiled header)
