# Generals/Code/GameEngine/Source/Common/System/Directory.cpp

## Purpose
This file implements directory traversal and file information retrieval functionalities for the Command & Conquer Generals game engine.

## Responsibilities
- Traverses directories to list files and subdirectories.
- Converts file times between `time_t` and `FILETIME`.
- Manages file and directory information using `FileInfo` and `Directory` classes.

## Key Types
- `FileInfo`: Stores information about a file, including name, size, attributes, and timestamps.
- `Directory`: Represents a directory and contains methods to list files and subdirectories.

## Key Functions
### TimetToFileTime
- Purpose: Converts a `time_t` value to a `FILETIME`.
- Calls: None

### FileTimeToTimet
- Purpose: Converts a `FILETIME` to a `time_t` value.
- Calls: None

### FileInfo::set
- Purpose: Initializes a `FileInfo` object from a `WIN32_FIND_DATA` structure.
- Calls: `FileTimeToTimet`

### Directory::Directory
- Purpose: Constructor that initializes the directory and populates file and subdirectory lists.
- Calls: `GetCurrentDirectory`, `SetCurrentDirectory`, `FindFirstFile`, `FindNextFile`, `FindClose`

### Directory::getFiles
- Purpose: Returns a pointer to the set of files in the directory.
- Calls: None

### Directory::getSubdirs
- Purpose: Returns a pointer to the set of subdirectories in the directory.
- Calls: None

## Globals
- None

## Dependencies
- `PreRTS.h`
- `Common/Directory.h`
- Windows API functions: `GetCurrentDirectory`, `SetCurrentDirectory`, `FindFirstFile`, `FindNextFile`, `FindClose`
