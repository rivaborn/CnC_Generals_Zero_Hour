# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/TARGA.CPP

## Purpose
Handles loading, saving, and manipulation of TGA (Targa) image files.

## Responsibilities
- Read/write TGA files with support for palettes and truecolor images
- Handle TGA 2.0 extension data
- Compress/decompress image data using RLE
- Flip images horizontally/vertically
- Manage file I/O via WWLib or standard file APIs

## Key Types
- **Targa (Class)**: Main class for TGA file operations
- **TGAHeader (Struct)**: Contains TGA file header information
- **TGA2Extension (Struct)**: Stores TGA 2.0 extension data
- **TGA2Footer (Struct)**: Contains TGA 2.0 footer signature

## Key Functions
### Targa::Open
- Purpose: Opens a TGA file and reads its header
- Calls: File_Open_Read, File_Seek, File_Read

### Targa::Load
- Purpose: Loads TGA image data into provided buffers
- Calls: Open, File_Read, DecodeImage

### Targa::DecodeImage
- Purpose: Decompresses RLE-encoded TGA image data
- Calls: File_Read

### Targa::EncodeImage
- Purpose: Compresses image data using TGA RLE algorithm
- Calls: File_Write, malloc, free

### Targa::InvertImage
- Purpose: Inverts color channels in truecolor images
- Calls: None

## Globals
- **TGAFile (FileClass*)**: File handle for WWLib file operations
- **mFH (int)**: File handle for standard file operations
- **Header (TGAHeader)**: Current TGA file header
- **mExtension (TGA2Extension)**: TGA 2.0 extension data

## Dependencies
- Key includes: `targa.h`, `wwfile.h`, `ffactory.h`, `stdio.h`, `malloc.h`, `memory.h`, `string.h`
- External symbols: `_TheFileFactory`, `_TheWritingFileFactory`, `WWDEBUG_SAY`
