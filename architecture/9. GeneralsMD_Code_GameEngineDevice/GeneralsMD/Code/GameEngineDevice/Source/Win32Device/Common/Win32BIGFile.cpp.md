# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/Common/Win32BIGFile.cpp

## Purpose
Handles file operations for BIG archive files on Windows, providing access to archived game resources.

## Responsibilities
- Opens files from BIG archives (read/write)
- Manages file info retrieval for archived files
- Handles streaming vs. RAM-based file access
- Provides basic file system operations (close, name/path access)

## Key Types
- **Win32BIGFile (Class)**: Main class for BIG file operations
- **ArchivedFileInfo (Struct)**: Not defined here, used for file metadata

## Key Functions
### `openFile`
- Purpose: Opens a file from the BIG archive with specified access flags
- Calls: `getArchivedFileInfo`, `newInstance`, `openFromArchive`, `copyDataToFile`, `close`, `TheLocalFileSystem->openFile`

### `getFileInfo`
- Purpose: Retrieves file information for files in the BIG archive
- Calls: `getArchivedFileInfo`, `TheLocalFileSystem->getFileInfo`

## Globals
- **TheLocalFileSystem (External)**: Used to access local file system operations

## Dependencies
- `Common/LocalFile.h`, `Common/LocalFileSystem.h`, `Common/RAMFile.h`, `Common/StreamingArchiveFile.h`, `Common/GameMemory.h`, `Common/PerfTimer.h`, `Win32Device/Common/Win32BIGFile.h`
- `AsciiString`, `File`, `FileInfo`, `ArchivedFileInfo` (external types)
