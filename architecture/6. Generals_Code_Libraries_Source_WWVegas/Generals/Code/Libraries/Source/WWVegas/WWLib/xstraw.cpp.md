# Generals/Code/Libraries/Source/WWVegas/WWLib/xstraw.cpp

## Purpose
Implements data reading abstractions for buffer and file sources via `BufferStraw` and `FileStraw` classes.

## Responsibilities
- Provides buffered data access via `BufferStraw`
- Handles file I/O via `FileStraw`
- Manages resource cleanup (file closing)
- Supports incremental data reading

## Key Types
- `BufferStraw` (Class): reads data from an in-memory buffer
- `FileStraw` (Class): reads data from a file
- `HasOpened` (bool): tracks if `FileStraw` opened the file

## Key Functions
### `BufferStraw::Get`
- Purpose: Copies data from internal buffer to caller's buffer
- Calls: `BufferPtr.Get_Size()`, `BufferPtr.Get_Buffer()`, `memmove`

### `FileStraw::Get`
- Purpose: Reads data from file into caller's buffer
- Calls: `Valid_File()`, `File->Is_Open()`, `File->Is_Available()`, `File->Open()`, `File->Read()`

### `FileStraw::~FileStraw`
- Purpose: Cleans up file resources if opened by this instance
- Calls: `Valid_File()`, `File->Close()`

## Globals
- None

## Dependencies
- `always.h`, `xstraw.h`, `<stddef.h>`, `<string.h>`
- `BufferPtr` (external), `FileClass` (external), `memmove`
