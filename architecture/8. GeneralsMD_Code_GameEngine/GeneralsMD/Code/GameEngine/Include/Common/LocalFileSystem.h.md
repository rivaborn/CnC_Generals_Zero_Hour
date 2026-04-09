# GeneralsMD/Code/GameEngine/Include/Common/LocalFileSystem.h

## Purpose
Defines the `LocalFileSystem` interface for file operations in the game engine.

## Responsibilities
- Declares pure virtual methods for file system operations
- Provides a singleton instance (`TheLocalFileSystem`)
- Inherits from `SubsystemInterface` for engine integration

## Key Types
- **File (Class)**: Represents an open file handle.
- **LocalFileSystem (Class)**: Abstract base class for local file system operations.
- **SubsystemInterface (Class)**: Base interface for engine subsystems.

## Key Functions
### `init`
- Purpose: Initialize the file system.
- Calls: None

### `reset`
- Purpose: Reset the file system state.
- Calls: None

### `update`
- Purpose: Update file system state (e.g., polling changes).
- Calls: None

### `openFile`
- Purpose: Open a file with specified access mode.
- Calls: None

### `doesFileExist`
- Purpose: Check if a file exists.
- Calls: None

### `getFileListInDirectory`
- Purpose: Retrieve files matching a pattern in a directory (optionally recursive).
- Calls: None

### `getFileInfo`
- Purpose: Get metadata (size, timestamps) for a file.
- Calls: None

### `createDirectory`
- Purpose: Create a new directory.
- Calls: None

## Globals
- **TheLocalFileSystem (LocalFileSystem*)**: Singleton instance of the local file system.

## Dependencies
- `Common/SubsystemInterface.h` (base class)
- `FileSystem.h` (typedefs, `FileInfo`, `FilenameList`)
- `File` class (forward-declared)
