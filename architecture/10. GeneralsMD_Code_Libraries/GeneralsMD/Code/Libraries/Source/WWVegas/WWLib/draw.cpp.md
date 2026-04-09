# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/draw.cpp

## Purpose
Provides low-level drawing functions for shapes and blocks on surfaces in the SAGE engine.

## Responsibilities
- Draw shapes from shape files onto surfaces
- Handle RLE-compressed and uncompressed shapes
- Perform block blitting with optional remapping
- Manage clipping windows and shape positioning

## Key Types
- `Surface`: destination drawing surface
- `ConvertClass`: pixel transformation converter
- `ShapeSet`: shape file data container
- `Blitter`: base class for blitting operations
- `RLEBlitter`: specialized blitter for RLE-compressed shapes
- `ShapeFlags_Type`: flags controlling draw behavior

## Key Functions
### Draw_Shape
- Purpose: Draws a shape from a shape file onto a surface
- Calls: `Set_Remap`, `Get_Rect`, `Get_Data`, `Get_Width`, `Get_Height`, `Is_RLE_Compressed`, `RLEBlitter_From_Flags`, `RLE_Blit`, `Blitter_From_Flags`, `Bit_Blit`

### Blit_Block
- Purpose: Blits a block of data from one surface to another
- Calls: `Set_Remap`, `Blitter_From_Flags`, `Bit_Blit`

## Globals
None

## Dependencies
- `always.h`, `blit.h`, `blitblit.h`, `blitter.h`, `bsurface.h`, `draw.h`, `dsurface.h`, `hsv.h`, `rlerle.h`, `shapeset.h`
- `Surface`, `ConvertClass`, `ShapeSet`, `Blitter`, `RLEBlitter`, `ShapeFlags_Type`, `Point2D`, `Rect`
