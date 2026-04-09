# Generals/Code/Libraries/Source/WWVegas/WWLib/xpipe.cpp

## Purpose
Implements pipe classes for buffered and file-based data streaming in the SAGE engine.

## Responsibilities
- Manages buffered data storage via `BufferPipe`
- Handles file I/O operations via `FilePipe`
- Provides pipe termination and cleanup logic
- Supports chained pipe operations

## Key Types
- `BufferPipe` (Class): Buffered pipe segment for in-memory data storage
- `FilePipe` (Class): File-based pipe for writing data to disk
- `Pipe` (Class, base): Abstract pipe interface (not shown in this file)

## Key Functions
### `BufferPipe::Put`
- Purpose: Writes data to an internal buffer, respecting buffer bounds
- Calls: `BufferPtr.Get_Size()`, `BufferPtr.Get_Buffer()`, `memmove`

### `FilePipe::End`
- Purpose: Closes the file and cleans up resources
- Calls: `Pipe::End()`, `File->Close()`

### `FilePipe::Put`
- Purpose: Writes data to a file, opening it if necessary
- Calls: `File->Is_Open()`, `File->Open()`, `File->Write()`

## Globals
- None

## Dependencies
- `always.h`, `xpipe.h`, `<stddef.h>`, `<string.h>`
- `BufferPtr` (external class), `FileClass` (external class)
