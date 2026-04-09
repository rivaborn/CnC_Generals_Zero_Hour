# GeneralsMD/Code/GameEngine/Include/Common/RAMFile.h

## Purpose
Defines the RAMFile class, a memory-mapped file abstraction for fast read/write operations.

## Responsibilities
- Memory-mapped file I/O operations
- File scanning utilities (int, float, string)
- File conversion and data copying
- Memory management for file data

## Key Types
- **RAMFile (Class)**: Memory-mapped file abstraction
- **RAMFileMagicEnum (Enum)**: Not inferable (line reference mismatch)
- **RAMFile_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (line reference mismatch)

## Key Functions
### RAMFile::open
- Purpose: Open a file for memory-mapped access
- Calls: Not inferable

### RAMFile::readEntireAndClose
- Purpose: Read entire file into memory and close
- Calls: Not inferable

### RAMFile::scanInt
- Purpose: Parse integer from current position
- Calls: Not inferable

### RAMFile::scanReal
- Purpose: Parse floating-point from current position
- Calls: Not inferable

### RAMFile::scanString
- Purpose: Parse string from current position
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/File.h` (base class)
- `AsciiString` (used in parameters)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
