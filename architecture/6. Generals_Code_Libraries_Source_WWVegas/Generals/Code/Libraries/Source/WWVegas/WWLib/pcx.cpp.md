# Generals/Code/Libraries/Source/WWVegas/WWLib/pcx.cpp

## Purpose
Reads PCX image files into a graphic buffer, supporting optional palette extraction.

## Responsibilities
- Parse PCX file headers and pixel data
- Handle RLE (Run-Length Encoding) decompression
- Manage memory allocation for image buffers
- Extract color palette if requested

## Key Types
- `PCX_HEADER` (struct): PCX file header structure
- `Surface` (type): Opaque surface handle
- `BSurface` (class): Internal surface implementation
- `PaletteClass` (class): Color palette container
- `FileClass` (class): File I/O wrapper

## Key Functions
### `Read_PCX_File`
- Purpose: Loads a PCX file into a surface buffer with optional palette extraction
- Calls: `file_handle.Read`, `file_handle.Seek`, `file_handle.Close`, `memset`, `W3DNEW`

## Globals
- `POOL_SIZE` (const): Buffer size for file reading (2048 bytes)
- `READ_CHAR()`/`READ_CHARx()` (macros): File reading with buffer refill logic

## Dependencies
- `pcx.h`, `always.h`, `<stdlib.h>`
- `GraphicBufferClass`, `Buffer`, `RGB` (external types)
- `W3DNEW` (memory allocation macro)
