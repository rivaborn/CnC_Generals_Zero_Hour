# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pcx.cpp

## Purpose
Reads PCX image files into a graphic buffer, supporting optional palette extraction and custom buffer allocation.

## Responsibilities
- Parses PCX file headers and validates format
- Decodes RLE-compressed PCX pixel data
- Handles optional palette extraction
- Manages memory allocation for image data

## Key Types
- `PCX_HEADER` (struct): Contains PCX file metadata (dimensions, format flags)
- `Surface` (pointer): Return type for loaded image data
- `BSurface` (class): Internal surface representation
- `Buffer` (class): Memory buffer wrapper

## Key Functions
### `Read_PCX_File`
- Purpose: Loads a PCX file into a surface buffer with optional palette extraction
- Calls:
  - `file_handle.Open/Read/Seek/Close`
  - `memset`
  - `W3DNEW` (operator)
  - `BSurface::Lock/Unlock`

## Globals
- `POOL_SIZE` (const): 2048 - Buffer size for file reading
- `pool` (char[2048]): Internal read buffer

## Dependencies
- `pcx.h` - Header definitions
- `always.h` - Common includes
- `stdlib.h` - Memory functions
- `FileClass`, `PaletteClass` - File I/O and color management
- `BSurface`, `Buffer` - Rendering primitives
