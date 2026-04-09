# GeneralsMD/Code/GameEngine/Source/Common/System/StreamingArchiveFile.cpp

## Purpose
Implements a streaming file interface for reading data from archives or files in a controlled manner.

## Responsibilities
- Manages file streaming operations (read, seek)
- Handles opening/closing files and archive entries
- Tracks current position and size within the stream
- Prevents writing to streaming files (read-only)

## Key Types
- **StreamingArchiveFile (Class)**: Main class for streaming file operations.
- **seekMode (Enum)**: Defines seek modes (START, CURRENT, END).

## Key Functions
### `open(const Char *filename, Int access)`
- Purpose: Opens a file using the file system.
- Calls: `TheFileSystem->openFile()`, `open(File *)`

### `openFromArchive(File *archiveFile, const AsciiString& filename, Int offset, Int size)`
- Purpose: Opens a file from an archive at a specific offset and size.
- Calls: `File::open()`, `m_file->seek()`

### `read(void *buffer, Int bytes)`
- Purpose: Reads data from the current position in the stream.
- Calls: `m_file->seek()`, `m_file->read()`

### `seek(Int pos, seekMode mode)`
- Purpose: Moves the current position in the stream.
- Calls: None (internal logic only).

## Globals
- **None**

## Dependencies
- `Common/AsciiString.h`
- `Common/FileSystem.h`
- `Common/StreamingArchiveFile.h`
- `Common/PerfTimer.h`
- `File` class (from file system)
- `TheFileSystem` (global file system instance)
