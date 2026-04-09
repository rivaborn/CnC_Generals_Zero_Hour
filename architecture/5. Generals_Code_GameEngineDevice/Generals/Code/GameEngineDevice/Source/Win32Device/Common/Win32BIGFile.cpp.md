# Generals/Code/GameEngineDevice/Source/Win32Device/Common/Win32BIGFile.cpp

## Purpose
Handles file operations for BIG archive files on Windows, providing access to archived game resources.

## Responsibilities
- Opens files from BIG archives with read/write access
- Manages file info retrieval for archived files
- Handles streaming vs. RAM-based file loading
- Provides basic file system operations for BIG files

## Key Types
- `Win32BIGFile` (Class): Main class for BIG file operations
- `ArchivedFileInfo` (Struct): Contains file metadata (offset, size, filename)
- `FileInfo` (Struct): Standard file information structure

## Key Functions
### `openFile`
- Purpose: Opens a file from the BIG archive with specified access flags
- Calls: `getArchivedFileInfo`, `newInstance`, `openFromArchive`, `copyDataToFile`, `close`

### `getFileInfo`
- Purpose: Retrieves file information for files in the BIG archive
- Calls: `getArchivedFileInfo`, `TheLocalFileSystem->getFileInfo`

## Globals
- `TheLocalFileSystem` (LocalFileSystem*): Reference to the local file system

## Dependencies
- `Common/LocalFile.h`, `Common/LocalFileSystem.h`, `Common/RAMFile.h`, `Common/StreamingArchiveFile.h`, `Common/GameMemory.h`, `Common/PerfTimer.h`, `Win32Device/Common/Win32BIGFile.h`
- `File`, `AsciiString`, `Bool`, `Int` types from engine framework
