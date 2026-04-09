# Generals/Code/Tools/Autorun/WSYS_file.h

## Purpose
Defines the `File` class for basic file operations in the WSYS library.

## Responsibilities
- Provides an interface for file I/O operations (read/write/seek).
- Manages file access modes (read/write/append/etc.).
- Handles file positioning and metadata (size/position).
- Supports formatted text output via `printf`.

## Key Types
- **File (Class)**: Abstract base class for file operations.
- **access (Enum)**: File access flags (READ, WRITE, APPEND, etc.).
- **seekMode (Enum)**: Seek position modes (START, CURRENT, END).

## Key Functions
### File::open
- Purpose: Opens a file with specified access flags.
- Calls: None (pure virtual in derived classes).

### File::read
- Purpose: Reads bytes from the file into a buffer.
- Calls: None (pure virtual in derived classes).

### File::write
- Purpose: Writes bytes from a buffer to the file.
- Calls: None (pure virtual in derived classes).

### File::seek
- Purpose: Sets the file position for read/write operations.
- Calls: None (pure virtual in derived classes).

### File::printf
- Purpose: Writes formatted text to the file.
- Calls: None (implementation in derived classes).

## Globals
- **IO_MAX_PATH (Int)**: Maximum allowable path length (2048).

## Dependencies
- `lib/basetype.h` (for `Char`, `Bool`, `Int` types).
- `FileSystem` class (friend, not shown in this file).
