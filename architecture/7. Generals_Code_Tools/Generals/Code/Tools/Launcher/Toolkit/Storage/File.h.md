# Generals/Code/Tools/Launcher/Toolkit/Storage/File.h

## Purpose
Defines a `File` class for file I/O operations on Windows, inheriting from `Stream`.

## Responsibilities
- File handling (open, close, create, delete)
- File I/O (read, write, seek)
- Error handling for file operations
- Stream interface implementation

## Key Types
- `File` (Class): Wraps Windows file operations with error handling.
- `EFileError` (Enum): File error codes (e.g., `FileError_FNF`, `FileError_Access`).

## Key Functions
### `Open`
- Purpose: Opens a file with specified rights.
- Calls: Windows API (`CreateFile`).

### `Load`
- Purpose: Loads file contents into a buffer.
- Calls: `GetLength`, `GetBytes`.

### `Save`
- Purpose: Writes data to the file.
- Calls: `PutBytes`.

### `OnFileError`
- Purpose: Handles file errors (retry logic).
- Calls: None (virtual hook).

## Globals
- `INVALID_HANDLE` (HANDLE): Represents an invalid file handle.

## Dependencies
- `<windows.h>` (Windows API)
- `Stream.h` (base class)
- `Rights.h` (file access rights)
- `UString.h` (string handling)
