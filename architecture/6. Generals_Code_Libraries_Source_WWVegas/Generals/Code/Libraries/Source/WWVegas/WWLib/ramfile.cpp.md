# Generals/Code/Libraries/Source/WWVegas/WWLib/ramfile.cpp

## Purpose
Implements a RAM-based file abstraction for in-memory data manipulation.

## Responsibilities
- Provides file-like operations (read/write/seek) on memory buffers
- Manages buffer allocation/deallocation
- Supports read/write/read-write access modes
- Handles automatic opening/closing for convenience

## Key Types
- RAMFileClass (Class): In-memory file abstraction with file-like operations
- None (other types)

## Key Functions
### RAMFileClass::Open(int access)
- Purpose: Opens the RAM file for read/write access
- Calls: None

### RAMFileClass::Read(void * buffer, int size)
- Purpose: Reads data from the RAM file into a buffer
- Calls: memmove

### RAMFileClass::Write(void const * buffer, int size)
- Purpose: Writes data from a buffer into the RAM file
- Calls: memmove

### RAMFileClass::Seek(int pos, int dir)
- Purpose: Changes the current read/write position in the RAM file
- Calls: None

## Globals
- None

## Dependencies
- "always.h", "ramfile.h", "string.h"
- memmove (from string.h)
- W3DNEWARRAY (memory allocation macro)
