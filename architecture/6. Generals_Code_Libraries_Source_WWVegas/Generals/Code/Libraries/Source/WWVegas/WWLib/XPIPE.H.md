# Generals/Code/Libraries/Source/WWVegas/WWLib/XPIPE.H

## Purpose
Defines pipe terminators for storing data into memory buffers or files in the SAGE engine's data processing pipeline.

## Responsibilities
- Provides `BufferPipe` for writing data to memory buffers
- Provides `FilePipe` for writing data to files
- Implements `Put()` and `End()` methods for data handling
- Manages buffer/file state and validation

## Key Types
- **BufferPipe (class)**: Pipe terminator that writes data to a memory buffer
- **FilePipe (class)**: Pipe terminator that writes data to a file
- **Pipe (class)**: Base class (external)

## Key Functions
### BufferPipe::Put
- Purpose: Writes data to the internal buffer
- Calls: `BufferPtr.Is_Valid()`

### FilePipe::Put
- Purpose: Writes data to the file
- Calls: `Valid_File()`

### FilePipe::End
- Purpose: Finalizes file writing
- Calls: None

## Globals
- None

## Dependencies
- `buff.h` (Buffer class)
- `pipe.h` (Pipe base class)
- `wwfile.h` (FileClass)
