# Generals/Code/GameEngine/Source/Common/System/ArchiveFileSystem.cpp

## Purpose
This file implements the `ArchiveFileSystem` class, which manages archive files and provides functionality to load, search, and access files within these archives.

## Responsibilities
- Manages archive files and their contents.
- Loads archive files into a directory tree structure.
- Provides methods to check if a file exists, open a file, get file information, and retrieve the archive filename for a given file.
- Handles loading of mods from specified directories or BIG files.

## Key Types
- `ArchiveFileSystem` (Class): Manages archive files and their contents.
- `ArchivedDirectoryInfo` (Struct): Represents directory information within an archive.
- `ArchivedFileLocationMap` (Type): Maps filenames to their archive locations.

## Key Functions
### ArchiveFileSystem::loadIntoDirectoryTree
- Purpose: Loads the contents of an archive file into a directory tree structure.
- Calls:
  - `ArchiveFile::getFileListInDirectory`
  - `AsciiString::toLower`
  - `AsciiString::tokenize`

### ArchiveFileSystem::loadMods
- Purpose: Loads mods from specified directories or BIG files into the archive file system.
- Calls:
  - `openArchiveFile`
  - `loadIntoDirectoryTree`
  - `loadBigFilesFromDirectory`

### ArchiveFileSystem::doesFileExist
- Purpose: Checks if a specified file exists within the archive file system.
- Calls:
  - `AsciiString::toLower`
  - `AsciiString::tokenize`

### ArchiveFileSystem::openFile
- Purpose: Opens a specified file from the archive file system.
- Calls:
  - `getArchiveFilenameForFile`
  - `ArchiveFile::openFile`

### ArchiveFileSystem::getFileInfo
- Purpose: Retrieves information about a specified file within the archive file system.
- Calls:
  - `getArchiveFilenameForFile`
  - `ArchiveFile::getFileInfo`

### ArchiveFileSystem::getArchiveFilenameForFile
- Purpose: Determines the archive filename for a given file.
- Calls:
  - `AsciiString::toLower`
  - `AsciiString::tokenize`

### ArchiveFileSystem::getFileListInDirectory
- Purpose: Retrieves a list of filenames in a specified directory within the archive file system.
- Calls:
  - `ArchiveFile::getFileListInDirectory`

## Globals
- `TheArchiveFileSystem` (ArchiveFileSystem*): Global instance of the archive file system.

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/ArchiveFile.h"
  - "Common/ArchiveFileSystem.h"
  - "Common/AsciiString.h"
  - "Common/PerfTimer.h"

- External symbols used but not defined here:
  - `TheGlobalData`
  - `DEBUG_LOG`
  - `DEBUG_ASSERTLOG`
