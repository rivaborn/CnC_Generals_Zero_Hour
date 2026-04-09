# Generals/Code/Tools/Autorun/WSYS_StdFileSystem.cpp

## Purpose
Implements a standard file system interface for the WSYS library, providing basic file operations.

## Responsibilities
- Manages file opening via `StdFile` objects
- Handles file cleanup (delete-on-close)
- Provides a simple file system abstraction

## Key Types
- `StdFileSystem` (Class): File system interface implementation
- `StdFile` (Class): Underlying file object (included from header)

## Key Functions
### `StdFileSystem::~StdFileSystem`
- Purpose: Destructor for `StdFileSystem`
- Calls: None

### `StdFileSystem::open`
- Purpose: Opens a file and returns a `File` pointer
- Calls: `new StdFile()`, `StdFile::open()`, `StdFile::deleteOnClose()`, `delete`

## Globals
None

## Dependencies
- `wsys_StdFileSystem.h` (header)
- `wsys_StdFile.h` (header)
- `File` (external interface)
- `Char`, `Int` (types)
