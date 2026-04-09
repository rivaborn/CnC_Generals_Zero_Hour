# GeneralsMD/Code/GameEngine/Include/Common/Directory.h

## Purpose
Provides classes for directory traversal and file information retrieval on Windows.

## Responsibilities
- Encapsulates Windows directory enumeration via WIN32_FIND_DATA
- Stores file metadata (name, timestamps, attributes, size)
- Manages sets of files and subdirectories
- Compares files by filename for sorting

## Key Types
- FileInfo (class): stores metadata for a single file
- FileInfoComparator (struct): defines comparison for FileInfo sorting
- Directory (class): represents a directory and its contents

## Key Functions
### FileInfo::set
- Purpose: Populates FileInfo from WIN32_FIND_DATA
- Calls: Not inferable

### Directory::getFiles
- Purpose: Returns set of files in directory
- Calls: Not inferable

### Directory::getSubdirs
- Purpose: Returns set of subdirectories
- Calls: Not inferable

## Globals
None

## Dependencies
- Common/AsciiString.h
- Common/STLTypedefs.h
- WIN32_FIND_DATA (Windows API)
- std::set (STL)
