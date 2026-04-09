# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/xpipe.cpp

## Purpose
Implements pipe classes for buffered and file-based data streaming in the SAGE engine.

## Responsibilities
- Manages buffered data storage via `BufferPipe`
- Handles file I/O operations via `FilePipe`
- Provides pipe termination and cleanup logic
- Supports chained pipe operations

## Key Types
- `BufferPipe` (Class): Buffered pipe segment that stores data in memory
- `FilePipe` (Class): Pipe that writes data to a file
- `Pipe` (Class, base): Abstract pipe interface (not shown in this file)

## Key Functions
### `BufferPipe::Put`
- Purpose: Writes data to an internal buffer
- Calls: `BufferPtr.Get_Size()`, `BufferPtr.Get_Buffer()`, `memmove`

### `FilePipe::End`
- Purpose: Closes the file and cleans up resources
- Calls: `Pipe::End()`, `File->Close()`

### `FilePipe::Put`
- Purpose: Writes data to a file, opening it if needed
- Calls: `File->Is_Open()`, `File->Open()`, `File->Write()`

## Globals
- None

## Dependencies
- `always.h`, `xpipe.h`, `<stddef.h>`, `<string.h>`
- `BufferPtr` (class), `File` (class), `FileClass` (enum)
