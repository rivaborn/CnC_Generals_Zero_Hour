# GeneralsMD/Code/GameEngine/Source/Common/System/Directory.cpp

## Purpose
Handles directory traversal and file information retrieval on Windows.

## Responsibilities
- Converts between time_t and FILETIME
- Populates FileInfo objects from WIN32_FIND_DATA
- Recursively scans directories for files and subdirectories
- Manages current directory state during traversal

## Key Types
- FileInfo (struct): stores file metadata (name, timestamps, size, attributes)
- Directory (class): wraps directory traversal logic

## Key Functions
### TimetToFileTime
- Purpose: Converts time_t to FILETIME
- Calls: Int32x32To64

### FileTimeToTimet
- Purpose: Converts FILETIME to time_t
- Calls: None

### FileInfo::set
- Purpose: Initializes FileInfo from WIN32_FIND_DATA
- Calls: FileTimeToTimet

### Directory::Directory
- Purpose: Scans directory contents and populates file/subdirectory sets
- Calls: GetCurrentDirectory, SetCurrentDirectory, FindFirstFile, FindNextFile, FindClose

### Directory::getFiles
- Purpose: Returns set of files in directory
- Calls: None

### Directory::getSubdirs
- Purpose: Returns set of subdirectories
- Calls: None

## Globals
None

## Dependencies
- PreRTS.h
- Common/Directory.h
- Windows API (WIN32_FIND_DATA, FILETIME, etc.)
- AsciiString, FileInfoSet, DEBUG_LOG
