# GeneralsMD/Code/GameEngine/Source/Common/System/ArchiveFileSystem.cpp

## Purpose
Manages a virtual file system that loads files from archive files (BIG files) and provides access to them.

## Responsibilities
- Loads and indexes files from archive files into a directory tree structure
- Provides file existence checks and file opening functionality
- Supports mod loading from specified BIG files and directories
- Maintains a map of open archive files for quick access

## Key Types
- `ArchiveFileSystem` (Class): Main class that manages the virtual file system
- `ArchivedDirectoryInfo` (Struct): Represents a directory in the virtual file system
- `ArchivedFileLocationMap` (Type): Maps filenames to their archive locations

## Key Functions
### `loadIntoDirectoryTree`
- Purpose: Loads files from an archive into the directory tree structure
- Calls: `archiveFile->getFileListInDirectory`, `path.nextToken`, `dirInfo->m_directories.find`

### `loadMods`
- Purpose: Loads mod files from specified BIG files and directories
- Calls: `openArchiveFile`, `loadIntoDirectoryTree`, `loadBigFilesFromDirectory`

### `doesFileExist`
- Purpose: Checks if a file exists in the virtual file system
- Calls: `path.nextToken`, `dirInfo->m_directories.find`, `dirInfo->m_files.find`

### `openFile`
- Purpose: Opens a file from the virtual file system
- Calls: `getArchiveFilenameForFile`, `m_archiveFileMap[archiveFilename]->openFile`

### `getArchiveFilenameForFile`
- Purpose: Finds which archive file contains a given file
- Calls: `path.nextToken`, `dirInfo->m_directories.find`, `dirInfo->m_files.find`

## Globals
- `TheArchiveFileSystem` (ArchiveFileSystem*): Global instance of the archive file system

## Dependencies
- `ArchiveFile.h`, `ArchiveFileSystem.h`, `AsciiString.h`, `PerfTimer.h`
- `TheGlobalData` (external symbol)
- `DEBUG_LOG`, `DEBUG_ASSERTLOG` (logging macros)
