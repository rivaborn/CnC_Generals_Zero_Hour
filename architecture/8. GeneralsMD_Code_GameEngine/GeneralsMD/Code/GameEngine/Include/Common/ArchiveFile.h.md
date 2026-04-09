# GeneralsMD/Code/GameEngine/Include/Common/ArchiveFile.h

## Purpose
Defines the `ArchiveFile` class, an abstract interface for accessing files within archive files (e.g., mix files) in the SAGE engine.

## Responsibilities
- Provides virtual methods to query file info, open/close files, and manage archive file state.
- Manages a directory tree of archived files.
- Supports file listing and search operations within archives.
- Handles attachment of file objects and priority settings.

## Key Types
- **ArchiveFile (Class)**: Abstract base class for archive file operations.
- **File (Class)**: Reference to a file object (defined elsewhere).
- **FileInfo (Struct)**: Holds file metadata (external).
- **ArchivedFileInfo (Struct)**: Contains info about archived files (external).
- **DetailedArchivedDirectoryInfo (Struct)**: Represents directory structure in archives (external).
- **FilenameList (Type)**: List of filenames (external).

## Key Functions
### `ArchiveFile()`
- Purpose: Default constructor.
- Calls: None.

### `~ArchiveFile()`
- Purpose: Virtual destructor.
- Calls: None.

### `attachFile(File *file)`
- Purpose: Attaches a file object to the archive.
- Calls: None.

### `getFileListInDirectory(...)`
- Purpose: Populates a list of files matching a search pattern in a directory.
- Calls: None (implementation in derived class).

### `addFile(const AsciiString& path, const ArchivedFileInfo *fileInfo)`
- Purpose: Adds a file to the archive's directory tree.
- Calls: None.

### `getArchivedFileInfo(const AsciiString& filename)`
- Purpose: Retrieves `ArchivedFileInfo` for a given filename.
- Calls: None.

## Globals
None.

## Dependencies
- **Includes**:
