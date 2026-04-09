# GeneralsMD/Code/GameEngine/Source/Common/System/ArchiveFile.cpp

## Purpose
Manages archived files within a virtual filesystem structure, supporting directory traversal and wildcard-based file searches.

## Responsibilities
- Maintains a hierarchical directory structure of archived files
- Supports wildcard-based file searches using `*` and `?` patterns
- Provides file information lookup by path
- Handles file attachment/detachment for reading operations

## Key Types
- `ArchiveFile` (Class): Main class managing archived file system
- `DetailedArchivedDirectoryInfo` (Struct): Represents a directory with subdirectories and files
- `ArchivedFileInfo` (Struct): Contains metadata about an archived file

## Key Functions
### `SearchStringMatches`
- Purpose: Implements wildcard pattern matching for filenames
- Calls: Recursively calls itself for `*` wildcard handling

### `addFile`
- Purpose: Adds a file to the archive's directory structure
- Calls: `AsciiString::nextToken`, `AsciiString::toLower`

### `getFileListInDirectory`
- Purpose: Recursively collects filenames matching a search pattern
- Calls: `SearchStringMatches`, `getFileListInDirectory` (overload)

### `getArchivedFileInfo`
- Purpose: Retrieves file metadata by path
- Calls: `AsciiString::nextToken`, `AsciiString::toLower`

## Globals
- None

## Dependencies
- `ArchiveFile.h`, `ArchiveFileSystem.h`, `File.h`, `PerfTimer.h`
- `AsciiString`, `Bool`, `FilenameList` types
- `File` class for actual file I/O operations
