# Generals/Code/GameEngine/Source/Common/System/LocalFile.cpp

## Purpose
This file implements the `LocalFile` class, which provides functionality for reading from and writing to local files using both buffered and unbuffered I/O methods.

## Responsibilities
- Open and close files.
- Read from and write to files.
- Seek within files.
- Scan integers, reals, and strings from files.
- Convert file contents to RAM-based files.
- Read entire file content into a buffer and close the file.

## Key Types
- `LocalFile` (Class): Manages local file operations.
- None

## Key Functions
### LocalFile::open
- Purpose: Opens a file with specified access flags.
- Calls: `fopen`, `_open`

### LocalFile::close
- Purpose: Closes the current file if it is open.
- Calls: `fclose`, `_close`

### LocalFile::read
- Purpose: Reads data from the file into a buffer.
- Calls: `fread`, `_read`

### LocalFile::write
- Purpose: Writes data to the file from a buffer.
- Calls: `fwrite`, `_write`

### LocalFile::seek
- Purpose: Moves the file pointer to a specified position.
- Calls: `fseek`, `_lseek`

### LocalFile::scanInt
- Purpose: Scans and returns an integer from the file.
- Calls: `fread`, `_read`

### LocalFile::scanReal
- Purpose: Scans and returns a real number from the file.
- Calls: `fread`, `_read`

### LocalFile::scanString
- Purpose: Scans and returns a string from the file.
- Calls: `fread`, `_read`

### LocalFile::nextLine
- Purpose: Reads the next line from the file.
- Calls: `fread`, `_read`

### LocalFile::convertToRAMFile
- Purpose: Converts the current file to a RAM-based file.
- Calls: `newInstance`, `open`, `close`, `deleteInstance`

### LocalFile::readEntireAndClose
- Purpose: Reads the entire file content into a buffer and closes the file.
- Calls: `size`, `read`, `close`

## Globals
- `s_totalOpen` (Int): Tracks the number of open files.

## Dependencies
- Key includes:
  - `<stdio.h>`
  - `<fcntl.h>`
  - `<io.h>`
  - `<string.h>`
  - `<sys/stat.h>`
  - `<stdlib.h>`
  - `<ctype.h>`
  - `"Common/LocalFile.h"`
  - `"Common/RAMFile.h"`
  - `"Lib/BaseType.h"`
  - `"Common/PerfTimer.h"`

- External symbols used:
  - `fclose`, `_close`
  - `fread`, `_read`
  - `fwrite`, `_write`
  - `fseek`, `_lseek`
  - `atoi`, `atof`
