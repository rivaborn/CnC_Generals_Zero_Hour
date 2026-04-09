# Generals/Code/Tools/WW3D/max2w3d/TARGA.H

## Purpose
Header file defining the Targa class for reading/writing TGA image files.

## Responsibilities
- Defines TGA file format structures and constants
- Declares Targa class for TGA file I/O
- Provides error handling macros for TGA operations

## Key Types
- TGAHeader (struct): TGA file header structure
- TGA2Footer (struct): TGA 2.0 footer structure
- TGA2Extension (struct): TGA 2.0 extension area structure
- Targa (class): Main TGA file handling class

## Key Functions
### Targa::Open
- Purpose: Opens a TGA file in specified mode
- Calls: File_Open_Read, File_Open_Write, File_Open_ReadWrite

### Targa::Load
- Purpose: Loads TGA image data into memory
- Calls: Open, DecodeImage

### Targa::Save
- Purpose: Saves TGA image data to file
- Calls: Open, EncodeImage

### Targa::DecodeImage
- Purpose: Decodes compressed TGA image data
- Calls: Not inferable

### Targa::EncodeImage
- Purpose: Encodes TGA image data for writing
- Calls: Not inferable

## Globals
- TGA_ERROR_HANDLER (macro): Error handling macro for TGA operations
- TGAERR_* (constants): Error code definitions

## Dependencies
- FileClass (conditional): WWLIB file handling class
- Standard C file I/O functions (when TGA_USES_WWLIB_FILE_CLASSES not defined)
