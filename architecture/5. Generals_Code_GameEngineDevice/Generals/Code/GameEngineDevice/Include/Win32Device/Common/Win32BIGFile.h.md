# Generals/Code/GameEngineDevice/Include/Win32Device/Common/Win32BIGFile.h

## Purpose
Header for Win32BIGFile class, which handles BIG file operations on Windows platforms.

## Responsibilities
- Manages BIG file access and file operations
- Provides file info retrieval and file opening/closing
- Handles BIG file search priority and path management

## Key Types
- Win32BIGFile (Class): BIG file handler for Windows platform

## Key Functions
### Win32BIGFile()
- Purpose: Constructor for Win32BIGFile class
- Calls: None

### ~Win32BIGFile()
- Purpose: Destructor for Win32BIGFile class
- Calls: None

### getFileInfo()
- Purpose: Retrieves file information from BIG file
- Calls: None

### openFile()
- Purpose: Opens a file within the BIG file
- Calls: None

### closeAllFiles()
- Purpose: Closes all files opened in this BIG file
- Calls: None

### getName()
- Purpose: Returns the name of the BIG file
- Calls: None

### getPath()
- Purpose: Returns full path and name of BIG file
- Calls: None

### setSearchPriority()
- Purpose: Sets this BIG file's search priority
- Calls: None

### close()
- Purpose: Closes this BIG file
- Calls: None

## Globals
- None

## Dependencies
- ArchiveFile.h
- AsciiString.h
- List.h
