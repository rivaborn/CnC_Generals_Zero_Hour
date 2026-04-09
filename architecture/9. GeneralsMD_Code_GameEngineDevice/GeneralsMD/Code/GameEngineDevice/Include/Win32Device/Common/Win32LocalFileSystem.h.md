# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/Common/Win32LocalFileSystem.h

## Purpose
Win32-specific implementation of the LocalFileSystem interface for file operations on Windows.

## Responsibilities
- File I/O operations (open, read, write)
- File existence checks
- Directory listing and creation
- File metadata retrieval

## Key Types
- Win32LocalFileSystem (Class): Win32 implementation of LocalFileSystem abstract class

## Key Functions
### Win32LocalFileSystem()
- Purpose: Constructor for Win32LocalFileSystem
- Calls: None

### ~Win32LocalFileSystem()
- Purpose: Destructor for Win32LocalFileSystem
- Calls: None

### init()
- Purpose: Initialize the file system
- Calls: None

### reset()
- Purpose: Reset the file system state
- Calls: None

### update()
- Purpose: Update file system state
- Calls: None

### openFile()
- Purpose: Open a file with specified access mode
- Calls: None

### doesFileExist()
- Purpose: Check if a file exists
- Calls: None

### getFileListInDirectory()
- Purpose: Retrieve list of files matching search criteria in a directory
- Calls: None

### getFileInfo()
- Purpose: Get file metadata
- Calls: None

### createDirectory()
- Purpose: Create a directory
- Calls: None

## Globals
None

## Dependencies
- LocalFileSystem.h (base class interface)
- Common file system types (File, FileInfo, FilenameList, AsciiString)
