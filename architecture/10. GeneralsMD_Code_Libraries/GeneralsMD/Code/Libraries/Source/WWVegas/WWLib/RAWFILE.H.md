# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RAWFILE.H

## Purpose
Defines the `RawFileClass`, a low-level file I/O wrapper for the SAGE engine, handling platform-specific file operations.

## Responsibilities
- Abstracts platform-specific file I/O (Windows/Unix)
- Provides basic file operations (open, read, write, seek, etc.)
- Manages file handles and error handling
- Supports file biasing (sub-file access)

## Key Types
- **RawFileClass (Class)**: Low-level file I/O wrapper.
- **HANDLE_TYPE (Type)**: Platform-specific handle type (`FILE*` for Unix, `HANDLE` for Windows).

## Key Functions
### `RawFileClass::File_Name`
- Purpose: Returns the filename associated with the file object.
- Calls: None.

### `RawFileClass::Open`
- Purpose: Opens a file with specified access rights.
- Calls: `Set_Name`, `Create`, `Error`.

### `RawFileClass::Read`
- Purpose: Reads data from the file into a buffer.
- Calls: `Transfer_Block_Size`, `Raw_Seek`, `Error`.

### `RawFileClass::Write`
- Purpose: Writes data from a buffer to the file.
- Calls: `Transfer_Block_Size`, `Raw_Seek`, `Error`.

### `RawFileClass::Error`
- Purpose: Handles file I/O errors.
- Calls: None.

## Globals
- **NULL_HANDLE (Macro)**: Represents an invalid handle (`NULL` for Unix, `INVALID_HANDLE_VALUE` for Windows).
- **HANDLE_TYPE (Macro)**: Defines the handle type based on platform.

## Dependencies
- `wwfile.h`: Base `FileClass` definition.
- `wwstring.h`: String handling utilities.
- Platform-specific headers
