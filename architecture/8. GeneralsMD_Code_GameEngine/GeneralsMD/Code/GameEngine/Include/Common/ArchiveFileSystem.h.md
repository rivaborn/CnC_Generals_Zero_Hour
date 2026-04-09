# GeneralsMD/Code/GameEngine/Include/Common/ArchiveFileSystem.h

## Purpose
Defines the `ArchiveFileSystem` class and related structures for managing archive files and file operations in the game.

## Responsibilities
- Manages archive files and their contents
- Provides file operations (open, close, existence checks)
- Maintains directory structure and file metadata
- Handles mod loading and file searching

## Key Types
- `ArchivedDirectoryInfo` (Class): Represents a directory in an archive with subdirectories and files
- `DetailedArchivedDirectoryInfo` (Class): Extended directory info with file details
- `ArchivedFileInfo` (Class): Stores file metadata (name, archive, offset, size)
- `ArchiveFileSystem` (Class): Core class for archive file management

## Key Functions
### `openFile`
- Purpose: Opens a file from any archive
- Calls: Not inferable

### `doesFileExist`
- Purpose: Checks if a file exists in any archive
- Calls: Not inferable

### `getFileListInDirectory`
- Purpose: Searches for files matching a pattern in a directory
- Calls: Not inferable

## Globals
- `TheArchiveFileSystem` (ArchiveFileSystem*): Global instance of the archive file system

## Dependencies
- `SubsystemInterface.h`, `AsciiString.h`, `FileSystem.h`, `STLTypedefs.h`
- `File`, `ArchiveFile` (forward declarations)
