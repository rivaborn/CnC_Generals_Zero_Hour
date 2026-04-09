# Generals/Code/Libraries/Source/WWVegas/WWLib/ffactory.cpp

## Purpose
Implements file factory classes for managing file I/O operations, including path handling and file creation/cleanup.

## Responsibilities
- Manages file factory instances (default and writing)
- Handles file path manipulation (subdirectories, stripping)
- Implements file creation and cleanup via `Get_File`/`Return_File`
- Supports multi-path search for files
- Provides thread-safe subdirectory management

## Key Types
- `SimpleFileFactoryClass`: Manages file paths and subdirectories
- `RawFileFactoryClass`: Creates raw file instances
- `file_auto_ptr`: Smart pointer for file management

## Key Functions
### `Is_Full_Path`
- Purpose: Checks if a path is absolute (drive letter or UNC)
- Calls: None

### `SimpleFileFactoryClass::Get_File`
- Purpose: Creates and opens a file, handling path resolution
- Calls: `Is_Full_Path`, `BufferedFileClass` constructor, `Set_Name`, `Open`, `Close`

### `SimpleFileFactoryClass::Set_Sub_Directory`
- Purpose: Sets the current subdirectory for file operations
- Calls: `CriticalSectionClass::LockClass` (mutex)

## Globals
- `_DefaultFileFactory` (SimpleFileFactoryClass): Default file factory instance
- `_TheFileFactory` (FileFactoryClass*): Current file factory pointer
- `_DefaultWritingFileFactory` (RawFileFactoryClass): Default writing file factory
- `_TheWritingFileFactory` (RawFileFactoryClass*): Current writing file factory pointer

## Dependencies
- `ffactory.h`, `rawfile.h`, `bufffile.h`, `realcrc.h`
- `CriticalSectionClass`, `StringClass`, `W3DNEW` (memory allocation)
- Standard C library headers (`stdio.h`, `stdlib.h`, `assert.h`, `string.h`)
