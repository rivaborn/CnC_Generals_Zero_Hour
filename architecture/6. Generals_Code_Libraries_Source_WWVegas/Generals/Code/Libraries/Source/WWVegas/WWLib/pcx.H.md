# Generals/Code/Libraries/Source/WWVegas/WWLib/pcx.H

## Purpose
Defines structures and function declarations for reading and writing PCX image files.

## Responsibilities
- Define PCX header structure and RGB color structure
- Declare functions for PCX file I/O operations
- Provide interface for surface/palette manipulation with PCX format

## Key Types
- RGB (struct): Contains red, green, blue color components
- PCX_HEADER (struct): Contains PCX file header information including dimensions, palette, and encoding details

## Key Functions
### Read_PCX_File
- Purpose: Reads a PCX file and returns a surface with optional palette loading
- Calls: FileClass operations, Surface creation, PaletteClass operations

### Write_PCX_File
- Purpose: Writes a surface to a PCX file with optional palette inclusion
- Calls: FileClass operations, Surface access, PaletteClass operations

## Globals
None

## Dependencies
- bsurface.h: Surface class definitions
- palette.h: PaletteClass definitions
- wwfile.h: FileClass definitions
- string.h: Memory operations
