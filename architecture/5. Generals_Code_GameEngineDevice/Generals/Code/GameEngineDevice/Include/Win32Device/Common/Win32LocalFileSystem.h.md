# Generals/Code/GameEngineDevice/Include/Win32Device/Common/Win32LocalFileSystem.h

## Purpose
Win32-specific implementation of the LocalFileSystem interface for file operations.

## Responsibilities
- Implements file I/O operations for Windows
- Provides directory traversal and file existence checks
- Manages file handles and directory creation
- Supports file listing with wildcard patterns

## Key Types
- Win32LocalFileSystem (Class): Windows implementation of LocalFileSystem abstract class

## Key Functions
### Win32LocalFileSystem()
- Purpose: Constructor for Win32LocalFileSystem
- Calls: None

### ~Win32LocalFileSystem()
- Purpose: Destructor for Win32LocalFileSystem
- Calls: None

### init()
- Purpose: Initializes the file system
- Calls: None

### reset()
- Purpose: Resets the file system state
- Calls: None

### update()
- Purpose: Updates file system state
- Calls: None

### openFile()
- Purpose: Opens a file with specified access mode
- Calls: None

### doesFileExist()
- Purpose: Checks if a file exists
- Calls: None

### getFileListInDirectory()
- Purpose: Retrieves list of files matching a pattern in a directory
- Calls: None

### getFileInfo()
- Purpose: Gets file information
- Calls: None

### createDirectory()
- Purpose: Creates a directory
- Calls: None

## Globals
None

## Dependencies
- LocalFileSystem.h (base class interface)
- Common file system types (File, FileInfo, FilenameList, AsciiString)
