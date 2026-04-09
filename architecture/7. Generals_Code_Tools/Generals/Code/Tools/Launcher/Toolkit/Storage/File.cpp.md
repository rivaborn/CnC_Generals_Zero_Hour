# Generals/Code/Tools/Launcher/Toolkit/Storage/File.cpp

## Purpose
Provides cross-platform file I/O functionality for the SAGE engine, wrapping Win32 file operations.

## Responsibilities
- File opening/closing with access control (read/write)
- File position management (seeking, markers)
- Reading/writing bytes with error handling
- File availability checking and error reporting

## Key Types
- `File` (Class): Main file I/O wrapper
- `ERights` (Enum): File access mode (ReadOnly/WriteOnly/ReadWrite)
- `EFileError` (Enum): Error codes (FNF/Open/Read/Write/Seek/etc.)

## Key Functions
### `Open(ERights rights)`
- Purpose: Opens file with specified access rights
- Calls: `CreateFile`, `OnFileError`, `PrintWin32Error`

### `GetBytes(void* ptr, UInt32 bytes)`
- Purpose: Reads bytes from file
- Calls: `ReadFile`, `OnFileError`

### `PutBytes(const void* ptr, UInt32 bytes)`
- Purpose: Writes bytes to file
- Calls: `WriteFile`, `OnFileError`

### `OnFileError(EFileError error, bool canRetry)`
- Purpose: Handles file errors (debug output)
- Calls: `DebugPrint` (debug only)

## Globals
- `INVALID_HANDLE` (HANDLE): Win32 invalid handle constant

## Dependencies
- `<Debug/DebugPrint.h>` for error logging
- Win32 API: `CreateFile`, `ReadFile`, `WriteFile`, etc.
- `UString` for filename storage
