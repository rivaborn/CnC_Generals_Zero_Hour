# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/xstraw.cpp

## Purpose
Implements data reading abstractions for buffer and file sources via `BufferStraw` and `FileStraw` classes.

## Responsibilities
- Provides buffered data access via `BufferStraw`
- Handles file I/O via `FileStraw`
- Manages resource cleanup (file closing)
- Supports incremental data reading

## Key Types
- `BufferStraw` (Class): wraps a memory buffer for sequential reading
- `FileStraw` (Class): wraps a file handle for sequential reading
- `HasOpened` (bool): tracks whether `FileStraw` opened the file

## Key Functions
### `BufferStraw::Get`
- Purpose: Reads data from an internal buffer into a destination buffer
- Calls: `memmove`

### `FileStraw::Get`
- Purpose: Reads data from a file into a destination buffer
- Calls: `File->Is_Open`, `File->Is_Available`, `File->Open`, `File->Read`

### `FileStraw::~FileStraw`
- Purpose: Cleans up file resources if the straw opened the file
- Calls: `File->Close`

## Globals
None

## Dependencies
- `always.h`, `xstraw.h`, `<stddef.h>`, `<string.h>`
- `BufferPtr` (external), `FileClass` (external), `memmove`
