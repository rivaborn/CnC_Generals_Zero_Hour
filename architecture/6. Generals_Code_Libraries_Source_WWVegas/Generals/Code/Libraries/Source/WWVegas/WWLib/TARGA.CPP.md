# Generals/Code/Libraries/Source/WWVegas/WWLib/TARGA.CPP

## Purpose
Handles loading, saving, and manipulation of TGA (Targa) image files.

## Responsibilities
- Read/write TGA files with support for compression/decompression
- Manage image data and palettes
- Handle file I/O via platform-specific abstractions
- Support TGA 2.0 extension data

## Key Types
- Targa (Class): Main TGA file handler
- TGAHeader (Struct): TGA file header structure
- TGA2Extension (Struct): TGA 2.0 extension data
- TGA2Footer (Struct): TGA 2.0 footer structure

## Key Functions
### Targa::Open
- Purpose: Opens a TGA file and reads its header
- Calls: File_Open_Read, File_Seek, File_Read, Close

### Targa::Load
- Purpose: Loads TGA image data into provided buffers
- Calls: Open, File_Read, DecodeImage, InvertImage

### Targa::DecodeImage
- Purpose: Decompresses RLE-compressed TGA image data
- Calls: File_Read

### Targa::EncodeImage
- Purpose: Compresses image data using TGA RLE algorithm
- Calls: File_Write, malloc, free

### Targa::InvertImage
- Purpose: Inverts TrueColor image data (BGR to RGB conversion)
- Calls: None

## Globals
- None

## Dependencies
- targa.h (header)
- WWLib file classes (conditional)
- Standard C I/O (conditional)
- malloc.h, memory.h, string.h
- WWDEBUG_SAY for error reporting
