# Generals/Code/Tools/WW3D/max2w3d/TARGA.CPP

## Purpose
Handles TGA (Targa) image file operations including loading, saving, and compression/decompression.

## Responsibilities
- Read/write TGA files with support for palettes and truecolor images
- Handle TGA 2.0 extension data
- Implement RLE compression/decompression
- Manage file I/O through platform-specific abstractions

## Key Types
- `Targa` (Class): Main TGA file handler
- `TGAHeader` (Struct): TGA file header structure
- `TGA2Extension` (Struct): TGA 2.0 extension data
- `TGA2Footer` (Struct): TGA 2.0 footer data

## Key Functions
### `Targa::Open`
- Purpose: Opens a TGA file and reads its header
- Calls: `File_Open_Read`, `File_Seek`, `File_Read`, `Close`

### `Targa::Load`
- Purpose: Loads TGA image data into provided buffers
- Calls: `Open`, `File_Read`, `DecodeImage`, `InvertImage`

### `Targa::DecodeImage`
- Purpose: Decompresses RLE-compressed TGA image data
- Calls: `File_Read`

### `Targa::EncodeImage`
- Purpose: Compresses image data using TGA RLE algorithm
- Calls: `File_Write`, `malloc`, `free`

### `Targa::InvertImage`
- Purpose: Inverts color channels in truecolor images
- Calls: None

## Globals
- `TGAFile` (FileClass*): File handle (WWLib version)
- `mFH` (int): File handle (standard I/O version)
- `mImage` (char*): Image data buffer
- `mPalette` (char*): Palette data buffer
- `Header` (TGAHeader): Current file header
- `mExtension` (TGA2Extension): TGA 2.0 extension data

## Dependencies
- `targa.h`: Header file for TGA class
- `wwfile.h`, `ffactory.h`: WWLib file I/O classes
- Standard C I/O headers (`stdio.h`, `fcntl.h`, etc.) for non-WWLib builds
- Memory allocation functions (`malloc.h`, `memory.h`, `string.h`)
