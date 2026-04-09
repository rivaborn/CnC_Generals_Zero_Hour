# GeneralsMD/Code/GameEngine/Include/Common/file.h

## Purpose
Defines the `File` class, an abstract interface for basic file operations in the SAGE engine.

## Responsibilities
- Provides file I/O operations (read/write/seek)
- Manages file access modes (read/write/append/etc.)
- Supports text/binary file handling
- Handles file position and size queries
- Manages file object lifecycle

## Key Types
- **File (Class)**: Abstract base class for file operations.
- **access (Enum)**: File access flags (READ, WRITE, APPEND, etc.).
- **seekMode (Enum)**: Seek position modes (START, CURRENT, END).

## Key Functions
### `open`
- Purpose: Opens a file with specified access flags.
- Calls: None (pure virtual).

### `read`
- Purpose: Reads bytes from the file into a buffer.
- Calls: None (pure virtual).

### `write`
- Purpose: Writes bytes from a buffer to the file.
- Calls: None (pure virtual).

### `seek`
- Purpose: Sets the file position for next read/write.
- Calls: None (pure virtual).

### `readEntireAndClose`
- Purpose: Reads entire file into a buffer and closes it.
- Calls: None (pure virtual).

## Globals
- **None**

## Dependencies
- `lib/basetype.h` (base types)
- `Common/AsciiString.h` (string handling)
- `Common/GameMemory.h` (memory management)
