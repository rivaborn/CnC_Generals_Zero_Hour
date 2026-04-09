# Generals/Code/Libraries/Source/WWVegas/WWLib/bufffile.cpp

## Purpose
Implements a buffered file I/O class that extends `RawFileClass` to improve read performance by caching data in memory.

## Responsibilities
- Manages a buffer for file reads to reduce disk I/O
- Handles buffered and unbuffered read/write operations
- Maintains buffer state (offset, available bytes)
- Resets buffer on seek operations or file close

## Key Types
- `BufferedFileClass` (Class): Buffered file I/O wrapper
- `None`: No additional types defined

## Key Functions
### `Read`
- Purpose: Reads data from file with buffering optimization
- Calls: `BASECLASS::Read`, `memcpy`, `W3DNEWARRAY`

### `Write`
- Purpose: Writes data directly to file (bypasses buffer)
- Calls: `BASECLASS::Write`

### `Seek`
- Purpose: Repositions file pointer with buffer state management
- Calls: `BASECLASS::Seek`, `Reset_Buffer`

### `Reset_Buffer`
- Purpose: Frees buffer memory and resets state
- Calls: `delete []`

## Globals
- `_DesiredBufferSize` (int): Default buffer size for all instances

## Dependencies
- `RawFileClass` (base class)
- `W3DNEWARRAY` (memory allocation)
- `memcpy` (buffer copying)
- `wwdebug.h` (assertions)
