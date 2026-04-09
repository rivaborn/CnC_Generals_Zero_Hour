# Generals/Code/Tools/Autorun/WSYS_StdFile.cpp

## Purpose
Implements the `StdFile` class for file I/O operations using standard C file functions.

## Responsibilities
- Wraps standard C file operations (`open`, `read`, `write`, `seek`, `close`) for cross-platform compatibility.
- Manages file handles and access modes.
- Provides error handling for file operations.

## Key Types
- `StdFile` (Class): Wrapper for standard C file I/O operations.

## Key Functions
### `StdFile::StdFile()`
- Purpose: Default constructor initializes the file handle to -1.
- Calls: None.

### `StdFile::~StdFile()`
- Purpose: Destructor closes the file handle if open.
- Calls: `_close`, `File::close`.

### `StdFile::open()`
- Purpose: Opens a file with specified access flags.
- Calls: `File::open`, `_open`.

### `StdFile::close()`
- Purpose: Closes the current file.
- Calls: `File::close`.

### `StdFile::read()`
- Purpose: Reads data from the file into a buffer.
- Calls: `_read`.

### `StdFile::write()`
- Purpose: Writes data from a buffer to the file.
- Calls: `_write`.

### `StdFile::seek()`
- Purpose: Moves the file pointer to a specified position.
- Calls: `_lseek`.

## Globals
- None.

## Dependencies
- Key includes: `<stdio.h>`, `<fcntl.h>`, `<io.h>`, `<string.h>`, `<sys/stat.h>`, `"wsys_StdFile.h"`.
- External symbols: `_open`, `_close`, `_read`, `_write`, `_lseek`, `_O_CREAT`, `_O_TRUNC`, `_O_APPEND`, `_O_TEXT`, `_O_BINARY`, `_O_RDWR`, `_O_WRONLY`, `_O_RDONLY`, `_S_IREAD`, `_S_IWRITE`, `SEEK_SET`, `SEEK_CUR`, `SEEK_END`.
