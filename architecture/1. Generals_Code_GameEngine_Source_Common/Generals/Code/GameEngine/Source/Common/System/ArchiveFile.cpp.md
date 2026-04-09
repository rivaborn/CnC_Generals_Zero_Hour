# Generals/Code/GameEngine/Source/Common/System/ArchiveFile.cpp

## Purpose
This file implements the `ArchiveFile` class, which manages archive files in the game engine. It handles operations such as adding files, searching for files using wildcards, and retrieving file information.

## Responsibilities
- Manages archive files and their directories.
- Provides functionality to add files to the archive.
- Searches for files within the archive using wildcard patterns.
- Retrieves detailed information about archived files.

## Key Types
- `ArchiveFile` (Class): Manages archive files and directories.
- `DetailedArchivedDirectoryInfo` (Struct): Represents directory information in the archive.
- `ArchivedFileInfo` (Struct): Contains information about a specific file in the archive.

## Key Functions
### SearchStringMatches
- Purpose: Checks if a given string matches a search pattern with wildcards (`*` and `?`).
- Calls: None

### ArchiveFile::~ArchiveFile
- Purpose: Destructor for `ArchiveFile`, closes the associated file if open.
- Calls: `m_file->close()`

### ArchiveFile::addFile
- Purpose: Adds a file to the archive with its path and information.
- Calls: `AsciiString::toLower()`, `AsciiString::nextToken()`

### ArchiveFile::getFileListInDirectory (overloaded)
- Purpose: Retrieves a list of filenames matching a search pattern in a directory, optionally searching subdirectories.
- Calls: `SearchStringMatches`, recursive calls to itself

### ArchiveFile::attachFile
- Purpose: Attaches an external file to the archive.
- Calls: `m_file->close()`

### ArchiveFile::getArchivedFileInfo
- Purpose: Retrieves detailed information about a specific archived file.
- Calls: `AsciiString::toLower()`, `AsciiString::nextToken()`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/ArchiveFile.h"
  - "Common/ArchiveFileSystem.h"
  - "Common/File.h"
  - "Common/PerfTimer.h"

- External symbols used but not defined here:
  - `AsciiString` (class)
  - `Bool` (type)
  - `FilenameList` (type)
