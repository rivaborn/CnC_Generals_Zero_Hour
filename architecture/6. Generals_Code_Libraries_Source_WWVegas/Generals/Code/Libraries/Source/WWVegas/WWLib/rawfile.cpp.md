# Generals/Code/Libraries/Source/WWVegas/WWLib/rawfile.cpp

## Purpose
Implements the `RawFileClass` for file I/O operations, supporting cross-platform file handling with bias offsets, date/time manipulation, and error handling.

## Responsibilities
- File opening/closing with read/write permissions
- File operations (read/write/seek)
- File metadata (size, date/time)
- Bias manipulation for virtual file offsets
- Error handling and reporting

## Key Types
- `RawFileClass` (Class): Cross-platform file I/O wrapper with bias support
- `NULL_HANDLE` (Type): Platform-specific null handle value

## Key Functions
### `RawFileClass::Open`
- Purpose: Opens a file with specified access rights
- Calls: `Set_Name`, platform-specific file open functions

### `RawFileClass::Read`
- Purpose: Reads data from the file into a buffer
- Calls: Platform-specific read functions, `Error`

### `RawFileClass::Write`
- Purpose: Writes data from a buffer to the file
- Calls: Platform-specific write functions, `Error`

### `RawFileClass::Bias`
- Purpose: Sets virtual file offset and length
- Calls: `Size`, `Seek`

### `RawFileClass::Error`
- Purpose: Handles file errors with optional retry
- Calls: Platform-specific error reporting

## Globals
- `NULL_HANDLE` (void*): Platform-specific null handle

## Dependencies
- Platform-specific includes (`win.h`, `_UNIX` headers)
- Standard C libraries (`stdio.h`, `stdlib.h`, `string.h`)
- Custom headers (`always.h`, `rawfile.h`)
