# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/Common/Win32BIGFileSystem.h

## Purpose
Declares the Win32BIGFileSystem class, a Windows-specific implementation of the ArchiveFileSystem interface for handling BIG archive files.

## Responsibilities
- Manages BIG archive file operations on Windows
- Provides file loading and unloading functionality
- Implements archive file system initialization and updates
- Handles directory scanning for BIG files
- Manages file and archive file lifecycle

## Key Types
- Win32BIGFileSystem (Class): Windows implementation of archive file system for BIG files

## Key Functions
### Win32BIGFileSystem()
- Purpose: Constructor for Win32BIGFileSystem
- Calls: None

### ~Win32BIGFileSystem()
- Purpose: Destructor for Win32BIGFileSystem
- Calls: None

### init()
- Purpose: Initializes the file system
- Calls: None

### update()
- Purpose: Updates the file system state
- Calls: None

### reset()
- Purpose: Resets the file system state
- Calls: None

### postProcessLoad()
- Purpose: Performs post-load processing
- Calls: None

### closeAllArchiveFiles()
- Purpose: Closes all currently open archive files
- Calls: None

### openArchiveFile()
- Purpose: Opens an archive file by filename
- Calls: None

### closeArchiveFile()
- Purpose: Closes a specific archive file
- Calls: None

### closeAllFiles()
- Purpose: Closes all files associated with archive files
- Calls: None

### loadBigFilesFromDirectory()
- Purpose: Loads BIG files from a directory matching a file mask
- Calls: None

## Globals
None

## Dependencies
-
