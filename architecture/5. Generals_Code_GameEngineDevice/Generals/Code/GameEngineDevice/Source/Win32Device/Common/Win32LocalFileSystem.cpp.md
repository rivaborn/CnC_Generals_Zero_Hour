# Generals/Code/GameEngineDevice/Source/Win32Device/Common/Win32LocalFileSystem.cpp

## Purpose
Implements the Win32-specific local file system interface for the game engine.

## Responsibilities
- Manages file operations (open, read, write) on Windows
- Handles directory creation and file existence checks
- Supports recursive file listing in directories
- Provides file metadata retrieval (timestamps, sizes)

## Key Types
- `Win32LocalFileSystem` (Class): Win32 implementation of LocalFileSystem
- `FileInfo` (Struct): Contains file metadata (timestamps, sizes)

## Key Functions
### `openFile`
- Purpose: Opens a file with specified access flags
- Calls: `newInstance`, `createDirectory`, `Win32LocalFile::open`

### `doesFileExist`
- Purpose: Checks if a file exists on disk
- Calls: `_access`

### `getFileListInDirectory`
- Purpose: Recursively lists files in a directory matching a pattern
- Calls: `FindFirstFile`, `FindNextFile`, `FindClose`

### `getFileInfo`
- Purpose: Retrieves file metadata (timestamps, sizes)
- Calls: `FindFirstFile`, `FindClose`

### `createDirectory`
- Purpose: Creates a directory if it doesn't exist
- Calls: `CreateDirectory`

## Globals
None

## Dependencies
- Windows API (`windows.h`)
- `AsciiString`, `GameMemory`, `PerfTimer` (internal)
- `Win32LocalFileSystem.h`, `Win32LocalFile.h` (headers)
- `_access` (C runtime)
