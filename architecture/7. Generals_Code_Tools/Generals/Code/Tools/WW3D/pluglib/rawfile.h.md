# Generals/Code/Tools/WW3D/pluglib/rawfile.h

## Purpose
Defines the `RawFileClass`, a low-level file I/O abstraction for the SAGE engine, handling platform-specific file operations.

## Responsibilities
- Provides cross-platform file operations (open, read, write, seek, etc.)
- Manages file handles and bias ranges for sub-file access
- Supports file creation, deletion, and metadata (date/time)
- Handles error reporting and file attachment/detachment

## Key Types
- **RawFileClass (Class)**: Low-level file I/O wrapper with platform-specific handle management.
- **BASECLASS (Class)**: Alias for `FileClass` (base class).

## Key Functions
### `RawFileClass::Open`
- Purpose: Opens a file with specified access rights.
- Calls: Platform-specific handle creation (not visible in header).

### `RawFileClass::Read`
- Purpose: Reads data from the file into a buffer.
- Calls: Platform-specific read operations (not visible in header).

### `RawFileClass::Write`
- Purpose: Writes data from a buffer to the file.
- Calls: Platform-specific write operations (not visible in header).

### `RawFileClass::Bias`
- Purpose: Sets a sub-portion of the file to treat as the entire file.
- Calls: None (direct member variable assignment).

### `RawFileClass::Attach`
- Purpose: Attaches an existing file handle to this object.
- Calls: None (direct member variable assignment).

## Globals
- **None**

## Dependencies
- `wwfile.h` (base `FileClass` definition)
- Platform-specific headers (`stdio.h` for Unix, `win.h` for Windows)
- `osdep.h` (Unix-specific dependencies)
