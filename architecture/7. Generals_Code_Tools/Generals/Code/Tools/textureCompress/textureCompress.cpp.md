# Generals/Code/Tools/textureCompress/textureCompress.cpp

## Purpose
Texture compression tool for converting TGA textures to DDS format using NVIDIA's nvdxt utility.

## Responsibilities
- Scan source, target, and cache directories for texture files
- Determine which files need compression, copying, or deletion
- Invoke nvdxt to compress textures
- Manage file timestamps and permissions during operations

## Key Types
- **DebugMunkee (Class)**: Debug logging utility (Windows-only)
- **FileInfo (Class)**: Stores file metadata (name, timestamps, size, attributes)
- **FileInfoComparator (Struct)**: Comparison functor for FileInfo sorting
- **FileInfoSet (Type)**: Set of FileInfo objects sorted by filename
- **Directory (Class)**: Directory scanner that collects files and subdirectories

## Key Functions
### logStuff
- Purpose: Display log messages via console and MessageBox
- Calls: _vsnprintf, puts, MessageBox

### debugLog
- Purpose: Output debug messages to console, debug string, and log file
- Calls: OutputDebugString, puts, fputs

### scanDir
- Purpose: Main processing function that analyzes directories and determines file operations
- Calls: Directory constructor, eraseCachedFiles, copyCachedFiles, copyOrigFiles, compressOrigFiles

### compressOrigFiles
- Purpose: Compress TGA files to DDS using nvdxt and copy results
- Calls: CreateFile, WriteFile, system, CopyFile, _utime

### WinMain/main
- Purpose: Entry point that parses arguments and initiates processing
- Calls: usage, scanDir

## Globals
- **nodxtPrefix (const char**)**: Array of texture name prefixes that should skip compression
- **nodxtAnywhere (const char**)**: Array of substrings that should skip compression if found anywhere
- **theDebugMunkee (DebugMunkee**)**: Global debug logging instance

## Dependencies
- Windows API (windows.h, lmcons.h)
- C runtime (stdlib.h, stdio.h, string.h)
- STL containers (map, string, set)
- File system APIs (_io.h, sys/stat.h, sys/utime.h)
- External tool: nvdxt (NVIDIA texture compression utility)
