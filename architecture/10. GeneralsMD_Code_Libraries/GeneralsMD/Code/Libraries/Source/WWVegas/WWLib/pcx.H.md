# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pcx.H

## Purpose
Header file for PCX image format handling in the SAGE engine.

## Responsibilities
- Defines PCX file format structures and functions
- Provides PCX reading and writing functionality
- Integrates with Surface and Palette classes

## Key Types
- RGB (struct): Contains red, green, blue color components
- PCX_HEADER (struct): PCX file header structure with format metadata

## Key Functions
### Read_PCX_File
- Purpose: Reads a PCX file into a Surface object
- Calls: FileClass operations, Surface construction

### Write_PCX_File
- Purpose: Writes a Surface to a PCX file
- Calls: FileClass operations, Surface data access

## Globals
None

## Dependencies
- bsurface.h (Surface class)
- palette.h (PaletteClass)
- wwfile.h (FileClass)
- string.h (memcpy, memset)
