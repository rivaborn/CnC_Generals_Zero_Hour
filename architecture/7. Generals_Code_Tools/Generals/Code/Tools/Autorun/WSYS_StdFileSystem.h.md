# Generals/Code/Tools/Autorun/WSYS_StdFileSystem.h

## Purpose
Header file defining the `StdFileSystem` class, a concrete implementation of the `FileSystem` interface using `StdFile` objects.

## Responsibilities
- Provides a standard file system interface for file operations.
- Manages opening files via `StdFile` instances.
- Inherits core functionality from the base `FileSystem` class.

## Key Types
- **StdFileSystem (Class)**: Concrete file system implementation using `StdFile`.

## Key Functions
### `~StdFileSystem`
- Purpose: Virtual destructor for the `StdFileSystem` class.
- Calls: None.

### `open`
- Purpose: Opens a file and returns a `File` object.
- Calls: None (implementation not shown in header).

## Globals
- None.

## Dependencies
- **Includes**:
  - `wsys_File.h` (for `File` and `StdFile` definitions).
  - `wsys_FileSystem.h` (for `FileSystem` base class).
- **External Symbols**:
  - `FileSystem` (base class).
  - `File` (return type for `open`).
