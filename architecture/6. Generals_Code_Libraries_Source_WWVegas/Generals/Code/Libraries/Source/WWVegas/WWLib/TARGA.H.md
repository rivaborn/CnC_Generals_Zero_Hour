# Generals/Code/Libraries/Source/WWVegas/WWLib/TARGA.H

## Purpose
Header file defining the Targa class for reading/writing TGA image files.

## Responsibilities
- Define TGA file format structures and constants
- Declare Targa class for TGA file I/O
- Provide error handling macros for TGA operations

## Key Types
- TGAHeader (struct): TGA file header structure
- TGA2Footer (struct): TGA 2.0 footer structure
- TGA2Extension (struct): TGA 2.0 extension area structure
- Targa (class): Main TGA file handling class

## Key Functions
### Targa::Open
- Purpose: Open a TGA file in specified mode
- Calls: File_Open_Read, File_Open_Write, File_Open_ReadWrite

### Targa::Load
- Purpose: Load TGA image data into memory
- Calls: Open, DecodeImage

### Targa::Save
- Purpose: Save TGA image data to file
- Calls: Open, EncodeImage

### Targa::DecodeImage
- Purpose: Decode compressed TGA image data
- Calls: Not inferable

### Targa::EncodeImage
- Purpose: Encode TGA image data for writing
- Calls: Not inferable

## Globals
- TGAErrorHandler (macro): Error handling macro for TGA operations

## Dependencies
- FileClass (class): Used for file I/O operations
- Standard C file I/O functions (when TGA_USES_WWLIB_FILE_CLASSES is undefined)
