# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/TARGA.H

## Purpose
Header file defining the Targa class for reading/writing TGA image files.

## Responsibilities
- Define TGA file format structures (headers, extensions, timestamps)
- Declare Targa class for loading/saving TGA images
- Provide error handling macros for TGA operations
- Support both standard I/O and WWLib file classes

## Key Types
- `TGAHeader` (struct): TGA file header structure
- `TGA2Footer` (struct): TGA 2.0 footer structure
- `TGA2Extension` (struct): TGA 2.0 extension area
- `Targa` (class): Main TGA file handling class

## Key Functions
### `Targa::Open`
- Purpose: Opens a TGA file in specified mode
- Calls: File_Open_Read, File_Open_Write, File_Open_ReadWrite

### `Targa::Load`
- Purpose: Loads TGA image data into memory
- Calls: DecodeImage, InvertImage

### `Targa::Save`
- Purpose: Saves TGA image data to file
- Calls: EncodeImage

### `Targa::DecodeImage`
- Purpose: Decodes compressed TGA image data
- Calls: Not inferable

### `Targa::EncodeImage`
- Purpose: Encodes TGA image data for saving
- Calls: Not inferable

## Globals
- `TGA_USES_WWLIB_FILE_CLASSES` (define): Switches between I/O methods
- Error codes (TGAERR_*): Defines for error conditions

## Dependencies
- FileClass (class): Used when TGA_USES_WWLIB_FILE_CLASSES is defined
- Standard I/O functions (when using standard I/O)
