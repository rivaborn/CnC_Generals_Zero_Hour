# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/XSTRAW.H

## Purpose
Defines abstract data source classes (Straw) for buffer and file I/O in the SAGE engine.

## Responsibilities
- Provides `BufferStraw` for reading from memory buffers
- Provides `FileStraw` for reading from files
- Implements `Straw` interface for both data sources
- Manages buffer/file state and validity

## Key Types
- `BufferStraw` (Class): Wraps a memory buffer as a data source
- `FileStraw` (Class): Wraps a file as a data source
- `Straw` (Class, external): Base abstract data source class

## Key Functions
### `BufferStraw::Get`
- Purpose: Reads data from the internal buffer into the provided buffer
- Calls: `BufferPtr.Is_Valid()`

### `FileStraw::Get`
- Purpose: Reads data from the file into the provided buffer
- Calls: `Valid_File()`

### `FileStraw::~FileStraw`
- Purpose: Cleans up file resources
- Calls: Not inferable

## Globals
- None

## Dependencies
- `buff.h` (Buffer class)
- `straw.h` (Straw base class)
- `wwfile.h` (FileClass)
- `<stddef.h>` (size_t)
