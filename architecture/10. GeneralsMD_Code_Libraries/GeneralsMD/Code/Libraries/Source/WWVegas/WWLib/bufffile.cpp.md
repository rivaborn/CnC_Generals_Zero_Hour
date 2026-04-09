# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bufffile.cpp

## Purpose
Implements a buffered file I/O class that extends `RawFileClass` to improve read performance by caching data in memory.

## Responsibilities
- Manages a read buffer for file operations
- Provides buffered read/write/seek functionality
- Handles buffer allocation and cleanup
- Maintains buffer state (offset, available bytes)

## Key Types
- `BufferedFileClass` (Class): Buffered file I/O wrapper
- `None`: No additional types defined

## Key Functions
### `Read`
- Purpose: Reads data from file with buffering optimization
- Calls: `BASECLASS::Read`, `memcpy`

### `Write`
- Purpose: Writes data to file (bypasses buffer)
- Calls: `BASECLASS::Write`

### `Seek`
- Purpose: Repositions file pointer with buffer awareness
- Calls: `BASECLASS::Seek`, `Reset_Buffer`

### `Reset_Buffer`
- Purpose: Clears and deallocates the read buffer
- Calls: `delete []`

## Globals
- `_DesiredBufferSize` (int): Default buffer size (16KB)

## Dependencies
- `RawFileClass` (base class)
- `always.h`, `bufffile.h`, `wwdebug.h`, `string.h`
- `W3DNEWARRAY` macro
- `WWASSERT` macro
