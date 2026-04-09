# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ramfile.cpp

## Purpose
Implements a RAM-based file abstraction for in-memory data manipulation.

## Responsibilities
- Provides file-like operations (read/write/seek) on memory buffers
- Manages buffer allocation/deallocation
- Supports read/write/read-write access modes
- Handles virtual file positioning and sizing

## Key Types
- **RAMFileClass (Class)**: In-memory file abstraction with file-like operations
- **Access (Enum)**: File access modes (READ, WRITE, READ|WRITE)
- **SEEK_CUR/SEEK_SET/SEEK_END (Constants)**: Seek direction flags

## Key Functions
### RAMFileClass::Open(int access)
- Purpose: Opens the RAM file for specified access mode
- Calls: None

### RAMFileClass::Read(void *buffer, int size)
- Purpose: Reads data from the RAM file into a buffer
- Calls: memmove

### RAMFileClass::Write(void const *buffer, int size)
- Purpose: Writes data from a buffer to the RAM file
- Calls: memmove

### RAMFileClass::Seek(int pos, int dir)
- Purpose: Changes the current read/write position in the RAM file
- Calls: None

### RAMFileClass::Bias(int start, int length)
- Purpose: Adjusts the buffer's view to a sub-region
- Calls: None

## Globals
- None

## Dependencies
- **Includes**: always.h, ramfile.h, string.h
- **External**: W3DNEWARRAY (memory allocation), memmove (data copying)
- **Constants**: READ, WRITE, SEEK_CUR, SEEK_SET, SEEK_END (defined elsewhere)
