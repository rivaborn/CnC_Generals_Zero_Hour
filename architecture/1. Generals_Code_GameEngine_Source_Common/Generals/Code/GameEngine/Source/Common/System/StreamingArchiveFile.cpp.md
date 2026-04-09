# Generals/Code/GameEngine/Source/Common/System/StreamingArchiveFile.cpp

## Purpose
This file implements the `StreamingArchiveFile` class, which handles reading from files within an archive in a streaming manner.

## Responsibilities
- Manages opening and closing of files.
- Provides methods for reading data from files.
- Handles seeking within files.
- Supports opening files directly or from an archive.

## Key Types
- StreamingArchiveFile (Class): Manages file operations, including reading, writing, and seeking.

## Key Functions
### StreamingArchiveFile::StreamingArchiveFile
- Purpose: Constructor initializes member variables.
- Calls: None

### StreamingArchiveFile::~StreamingArchiveFile
- Purpose: Destructor closes the file if it is open.
- Calls: File::close()

### StreamingArchiveFile::open
- Purpose: Opens a file using standard C open() call or from an archive.
- Calls: TheFileSystem->openFile(), File::open(), m_file->seek()

### StreamingArchiveFile::read
- Purpose: Reads data from the file into a buffer.
- Calls: m_file->seek(), m_file->read()

### StreamingArchiveFile::write
- Purpose: Writes data to the file (not supported for streaming files).
- Calls: DEBUG_CRASH()

### StreamingArchiveFile::seek
- Purpose: Moves the current position within the file.
- Calls: None

## Globals
- None

## Dependencies
- Key includes:
  - `stdio.h`
  - `fcntl.h`
  - `io.h`
  - `string.h`
  - `sys/stat.h`
  - "Common/AsciiString.h"
  - "Common/FileSystem.h"
  - "Common/StreamingArchiveFile.h"
  - "Common/PerfTimer.h"
