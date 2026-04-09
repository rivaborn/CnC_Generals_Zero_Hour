# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/Common/Win32BIGFileSystem.cpp

## Purpose
Implements the Windows-specific BIG file system for loading and managing archive files in Generals Zero Hour.

## Responsibilities
- Loads and parses BIG archive files from directories
- Manages archive file opening/closing
- Integrates with the local file system for asset loading
- Handles music archive shutdown for audio cleanup

## Key Types
- `Win32BIGFileSystem` (Class): Manages BIG archive file operations
- `BIGFileIdentifier` (const char*): Identifier string for BIG files ("BIGF")

## Key Functions
### `init`
- Purpose: Initializes the BIG file system and loads BIG files from directories
- Calls: `loadBigFilesFromDirectory`, `GetStringFromGeneralsRegistry`

### `openArchiveFile`
- Purpose: Opens and parses a BIG archive file
- Calls: `TheLocalFileSystem->openFile`, `NEW Win32BIGFile`, `fp->read`, `fp->seek`, `archiveFile->addFile`, `archiveFile->attachFile`

### `closeArchiveFile`
- Purpose: Closes a specific BIG archive file and cleans up resources
- Calls: `TheAudio->stopAudio`, `delete`

### `loadBigFilesFromDirectory`
- Purpose: Loads all BIG files matching a mask from a directory
- Calls: `TheLocalFileSystem->getFileListInDirectory`, `openArchiveFile`, `loadIntoDirectoryTree`

## Globals
- `BIGFileIdentifier` (const char*): String identifier for BIG files

## Dependencies
- `Win32BIGFile.h`, `ArchiveFileSystem.h`, `LocalFileSystem.h`, `registry.h`
- `TheLocalFileSystem`, `TheAudio` (external globals)
- Winsock2.h for network byte order functions
