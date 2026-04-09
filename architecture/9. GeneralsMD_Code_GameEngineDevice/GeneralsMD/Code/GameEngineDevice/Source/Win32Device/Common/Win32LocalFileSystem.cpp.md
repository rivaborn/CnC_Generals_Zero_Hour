# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/Common/Win32LocalFileSystem.cpp

## Purpose
Implements Windows-specific file system operations for the game engine.

## Responsibilities
- Manages file opening, directory creation, and file existence checks
- Supports recursive directory traversal for file listing
- Provides file metadata retrieval (timestamps, sizes)
- Handles Win32-specific file operations

## Key Types
- `Win32LocalFileSystem` (Class): Windows implementation of LocalFileSystem
- `FileInfo` (Struct): Contains file metadata (timestamps, sizes)

## Key Functions
### `openFile`
- Purpose: Opens a file with specified access flags
- Calls: `newInstance`, `createDirectory`, `Win32LocalFile::open`

### `doesFileExist`
- Purpose: Checks if a file exists on disk
- Calls: `_access`

### `getFileListInDirectory`
- Purpose: Recursively lists files in directories matching a pattern
- Calls: `FindFirstFile`, `FindNextFile`, `FindClose`

### `getFileInfo`
- Purpose: Retrieves file metadata (timestamps, sizes)
- Calls: `FindFirstFile`, `FindClose`

### `createDirectory`
- Purpose: Creates a directory if it doesn't exist
- Calls: `CreateDirectory`

## Globals
- None

## Dependencies
- `<windows.h>` for Win32 API
- `AsciiString.h` for string handling
- `GameMemory.h` for memory management
- `Win32LocalFileSystem.h` for class definition
- `Win32LocalFile.h` for file operations
- `<io.h>` for `_access` function
