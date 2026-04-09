# Generals/Code/GameEngineDevice/Include/Win32Device/Common/Win32BIGFileSystem.h

## Purpose
Defines the Win32BIGFileSystem class, a Windows-specific implementation of the ArchiveFileSystem interface for handling BIG archive files.

## Responsibilities
- Manages BIG archive files on Windows
- Provides file operations within archives
- Handles loading BIG files from directories
- Implements core file system interface methods

## Key Types
- Win32BIGFileSystem (Class): Windows-specific BIG file system implementation

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
- ArchiveFileSystem (base class)
- Char, Bool, AsciiString (types
