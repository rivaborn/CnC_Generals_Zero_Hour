# GeneralsMD/Code/GameEngine/Include/Common/FileSystem.h

## Purpose
Defines the FileSystem interface and related types for file I/O operations in the SAGE engine.

## Responsibilities
- Provides abstract file system operations (open, exist, list, info).
- Manages file paths and directories for game assets.
- Supports CD-based music file handling.
- Maintains a global file system instance.

## Key Types
- **File (Class)**: Abstract file handle interface.
- **FilenameList (Class)**: Set of filenames (case-insensitive).
- **FilenameListIter (Class)**: Iterator for FilenameList.
- **FileInfo (Struct)**: Contains file size and timestamp.
- **FileSystem (Class)**: Core file system interface.

## Key Functions
### FileSystem::openFile
- Purpose: Opens a file by name.
- Calls: Not inferable (virtual).

### FileSystem::doesFileExist
- Purpose: Checks if a file exists.
- Calls: Not inferable (virtual).

### FileSystem::getFileListInDirectory
- Purpose: Lists files in a directory matching a pattern.
- Calls: Not inferable (virtual).

### FileSystem::getFileInfo
- Purpose: Retrieves file metadata.
- Calls: Not inferable (virtual).

### FileSystem::createDirectory
- Purpose: Creates a directory.
- Calls: Not inferable (virtual).

## Globals
- **TheFileSystem (FileSystem*)**: Global file system instance.

## Dependencies
- `Common/File.h` (forward reference)
- `Common/STLTypedefs.h`
- `Common/SubsystemInterface.h`
- `<map>`, `<set>` (STL)
