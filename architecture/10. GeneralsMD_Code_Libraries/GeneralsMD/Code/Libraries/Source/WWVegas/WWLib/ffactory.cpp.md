# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ffactory.cpp

## Purpose
Implements file factory classes for file I/O operations in the SAGE engine, including path handling and file management.

## Responsibilities
- Manages file factory instances and global file factory pointers
- Implements file path manipulation (subdirectories, path stripping)
- Handles file opening/closing through factory pattern
- Provides thread-safe operations for file path management
- Supports both simple and raw file factory implementations

## Key Types
- `SimpleFileFactoryClass`: Manages file paths and subdirectories with thread safety
- `RawFileFactoryClass`: Basic file factory implementation
- `file_auto_ptr`: Smart pointer for automatic file management
- `CriticalSectionClass`: Thread synchronization for path operations

## Key Functions
### `Is_Full_Path`
- Purpose: Determines if a path is absolute (drive letter or UNC path)
- Calls: None

### `SimpleFileFactoryClass::Get_File`
- Purpose: Creates and opens a file with path resolution
- Calls: `Is_Full_Path`, `strrchr`, `strchr`, `strtok`, `BufferedFileClass` constructor

### `SimpleFileFactoryClass::Set_Sub_Directory`
- Purpose: Sets the current subdirectory with thread-safe locking
- Calls: `CriticalSectionClass::LockClass` constructor

### `SimpleFileFactoryClass::Prepend_Sub_Directory`
- Purpose: Prepends a directory to the search path with semicolon separation
- Calls: `CriticalSectionClass::LockClass` constructor

### `SimpleFileFactoryClass::Append_Sub_Directory`
- Purpose: Appends a directory to the search path with semicolon separation
- Calls: `CriticalSectionClass::LockClass` constructor

## Globals
- `_DefaultFileFactory` (SimpleFileFactoryClass): Default simple file factory instance
- `_TheFileFactory` (FileFactoryClass*): Global pointer to current file factory
- `_TheSimpleFileFactory` (SimpleFileFactoryClass*): Global pointer to simple file factory
- `_DefaultWritingFileFactory` (RawFileFactoryClass): Default writing file factory instance
- `_TheWritingFileFactory` (RawFileFactoryClass*): Global pointer to writing file factory

## Dependencies
- `ffactory.h`, `rawfile.h`, `bufffile.h`, `realcrc.h`
- `stdio.h`, `stdlib.h`, `assert.h`, `string.h`
- `StringClass`, `W3DNEW`, `WWASSERT` macros
- `CriticalSectionClass` for thread synchronization
