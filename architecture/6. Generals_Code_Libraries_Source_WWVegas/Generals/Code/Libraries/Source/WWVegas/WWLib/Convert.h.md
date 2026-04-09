# Generals/Code/Libraries/Source/WWVegas/WWLib/Convert.h

## Purpose
Defines the `ConvertClass` for converting 8-bit artwork pixels to screen pixel format with various blitting effects.

## Responsibilities
- Manages translation tables for pixel format conversion
- Provides blitter objects for different rendering effects (transparency, translucency, remapping)
- Handles both regular and RLE-compressed image blitting
- Supports dynamic remap table updates

## Key Types
- ShapeFlags_Type (Enum): Flags for different blitting effects (normal, translucent, remap, etc.)
- ConvertClass (Class): Main conversion class handling pixel format translation and blitting

## Key Functions
### Convert_Pixel
- Purpose: Converts a single source pixel to destination format
- Calls: None (inline function)

### Blitter_From_Flags
- Purpose: Returns appropriate blitter based on shape flags
- Calls: Not inferable

### RLEBlitter_From_Flags
- Purpose: Returns appropriate RLE blitter based on shape flags
- Calls: Not inferable

### Get_Translate_Table
- Purpose: Returns the translation table for manual pixel conversion
- Calls: None

### Set_Remap
- Purpose: Updates the remap table for remapping blitters
- Calls: None

## Globals
- None

## Dependencies
- `blitter.h` - Blitter class definitions
- `palette.h` - Palette class definitions
- `surface.h` - Surface class definitions
