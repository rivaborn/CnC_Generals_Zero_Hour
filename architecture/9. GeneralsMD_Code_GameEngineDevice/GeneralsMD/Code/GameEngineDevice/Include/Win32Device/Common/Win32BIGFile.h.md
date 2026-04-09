# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/Common/Win32BIGFile.h

## Purpose
Header for Win32BIGFile class, which handles BIG file operations on Windows platforms.

## Responsibilities
- Define Win32BIGFile class interface
- Declare BIG file manipulation methods
- Inherit from ArchiveFile base class

## Key Types
- Win32BIGFile (Class): Windows-specific BIG file handler

## Key Functions
### Win32BIGFile()
- Purpose: Constructor for Win32BIGFile
- Calls: None

### ~Win32BIGFile()
- Purpose: Destructor for Win32BIGFile
- Calls: None

### getFileInfo()
- Purpose: Retrieve file information from BIG file
- Calls: None

### openFile()
- Purpose: Open a file within the BIG file
- Calls: None

### closeAllFiles()
- Purpose: Close all open files in the BIG file
- Calls: None

### getName()
- Purpose: Get the BIG file name
- Calls: None

### getPath()
- Purpose: Get the full path and name of BIG file
- Calls: None

### setSearchPriority()
- Purpose: Set BIG file search priority
- Calls: None

### close()
- Purpose: Close the BIG file
- Calls: None

## Globals
- None

## Dependencies
- ArchiveFile.h
- AsciiString.h
- List.h
