# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Convert.h

## Purpose
Defines the `ConvertClass` for converting 8-bit artwork pixels to screen pixel format with various blitting effects.

## Responsibilities
- Manages pixel format conversion between source art and screen
- Provides blitter objects for different rendering effects (transparency, translucency, remapping)
- Maintains translation tables for fast pixel conversion
- Supports both regular and RLE-compressed image blitting

## Key Types
- `ShapeFlags_Type` (Enum): Flags for different blitting effects (normal, translucent, remap, etc.)
- `ConvertClass` (Class): Main conversion class handling pixel format translation and blitting

## Key Functions
### `Convert_Pixel`
- Purpose: Converts a single source pixel to destination format
- Calls: None (inline function)

### `Blitter_From_Flags`
- Purpose: Returns appropriate blitter based on shape flags
- Calls: Not visible in header

### `RLEBlitter_From_Flags`
- Purpose: Returns appropriate RLE blitter based on shape flags
- Calls: Not visible in header

### `Set_Remap`
- Purpose: Sets dynamic remap table for remapping blitters
- Calls: None

## Globals
- None

## Dependencies
- `blitter.h`, `palette.h`, `surface.h`
- `Blitter`, `RLEBlitter` classes (external)
- `PaletteClass`, `Surface` classes (external)
