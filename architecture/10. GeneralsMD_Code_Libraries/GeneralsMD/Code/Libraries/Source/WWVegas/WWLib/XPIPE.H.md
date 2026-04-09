# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/XPIPE.H

## Purpose
Defines pipe terminators for storing data into memory buffers or files in the SAGE engine's data processing pipeline.

## Responsibilities
- Provides `BufferPipe` for writing data to memory buffers.
- Provides `FilePipe` for writing data to files.
- Inherits from `Pipe` base class for pipeline integration.
- Handles buffer/file validation and data writing.

## Key Types
- `BufferPipe` (Class): Writes data to a memory buffer as the final pipe segment.
- `FilePipe` (Class): Writes data to a file as the final pipe segment.
- `Pipe` (Class, external): Base class for pipe segments.

## Key Functions
### `BufferPipe::Put`
- Purpose: Writes data to the internal buffer.
- Calls: `BufferPtr.Is_Valid()`

### `FilePipe::Put`
- Purpose: Writes data to the file.
- Calls: `Valid_File()`

### `FilePipe::End`
- Purpose: Finalizes file writing.
- Calls: None visible.

## Globals
- None

## Dependencies
- `buff.h` (Buffer class)
- `pipe.h` (Pipe base class)
- `wwfile.h` (FileClass)
