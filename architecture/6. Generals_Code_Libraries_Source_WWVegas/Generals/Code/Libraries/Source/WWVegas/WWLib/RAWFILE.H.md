# Generals/Code/Libraries/Source/WWVegas/WWLib/RAWFILE.H

## Purpose
Defines the `RawFileClass`, a low-level file I/O abstraction for the SAGE engine, handling platform-specific file operations.

## Responsibilities
- Provides cross-platform file I/O (Windows/Unix)
- Manages file handles, seeking, reading, and writing
- Supports file biasing (sub-file access)
- Handles file metadata (timestamps)
- Implements error reporting

## Key Types
- **RawFileClass (Class)**: Low-level file I/O wrapper with platform-specific handle management.
- **HANDLE_TYPE (Type)**: Platform-specific handle type (`FILE*` for Unix, `HANDLE` for Windows).

## Key Functions
### `RawFileClass::Open`
- Purpose: Opens a file with specified access rights.
- Calls: Platform-specific file open routines (not visible in header).

### `RawFileClass::Read`
- Purpose: Reads data from the file into a buffer.
- Calls: Platform-specific read routines (not visible in header).

### `RawFileClass::Write`
- Purpose: Writes data from a buffer to the file.
- Calls: Platform-specific write routines (not visible in header).

### `RawFileClass::Seek`
- Purpose: Changes the file position indicator.
- Calls: `Raw_Seek` (internal).

### `RawFileClass::Bias`
- Purpose: Restricts file access to a sub-portion (start/length).
- Calls: None (modifies internal state).

## Globals
- **NULL_HANDLE (Macro)**: Platform-specific null handle value.
- **WWERROR (Macro)**: Error code constant (-1).

## Dependencies
- `wwfile.h`: Base `FileClass` definition.
- Platform-specific headers (`stdio.h` for Unix, `win.h` for Windows).
- `osdep.h` (Unix-only).
