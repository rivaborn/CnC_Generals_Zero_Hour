# Generals/Code/Libraries/Source/WWVegas/WWLib/convert.cpp

## Purpose
Manages color conversion and blitting operations between art and screen palettes for rendering.

## Responsibilities
- Creates translation tables for color conversion
- Initializes blitter objects for different rendering modes
- Provides methods to select appropriate blitters based on shape flags
- Handles both 8-bit and 16-bit color formats
- Manages RLE-aware blitters for compressed shapes

## Key Types
- ConvertClass (Class): Main conversion manager handling palette translation and blitting
- Blitter (Class): Base class for blitting operations (external)
- RLEBlitter (Class): Base class for RLE-aware blitting (external)
- PaletteClass (Class): Represents color palettes (external)
- Surface (Class): Represents display surfaces (external)

## Key Functions
### ConvertClass::ConvertClass
- Purpose: Initializes conversion tables and blitters based on palette and surface format
- Calls: W3DNEW, W3DNEWARRAY, artpalette.Closest_Color, screenpalette.Closest_Color, ((DSurface &)surface).Build_Remap_Table, ((DSurface &)surface).Get_Halfbright_Mask, ((DSurface &)surface).Get_Quarterbright_Mask

### ConvertClass::~ConvertClass
- Purpose: Cleans up allocated resources
- Calls: delete for all blitter objects and translation tables

### ConvertClass::Blitter_From_Flags
- Purpose: Returns appropriate blitter based on shape rendering flags
- Calls: None

### ConvertClass::RLEBlitter_From_Flags
- Purpose: Returns appropriate RLE-aware blitter based on shape rendering flags
- Calls: None

## Globals
None

## Dependencies
- always.h, blitblit.h, convert.h, dsurface.h, hsv.h, rlerle.h
- BlitPlainXlat, BlitTransXlat, BlitTransZRemapXlat, BlitTransRemapDest, BlitTransRemapXlat, BlitTransLucent75, BlitTransLucent50, BlitTransLucent25 (external blitter classes)
- RLEBlitTransXlat, RLEBlitTransZRemapXlat, RLEBlitTransRemapDest, RLEBlitTransRemapXlat, RLEBlitTransLucent75, RLEBlitTransLucent50, RLEBlitTransLucent25 (external RLE blitter classes)
- W3DNEW, W3DNEWARRAY (memory allocation macros)
- PaletteClass, Surface, DSurface (external classes)
