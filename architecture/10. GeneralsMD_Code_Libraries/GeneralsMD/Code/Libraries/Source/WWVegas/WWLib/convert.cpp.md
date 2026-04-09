# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/convert.cpp

## Purpose
Manages color conversion and blitting operations between art and screen palettes for rendering.

## Responsibilities
- Constructs translation and shadow tables for palette conversion
- Creates blitter objects for various rendering effects (transparency, translucency, remapping)
- Provides methods to select appropriate blitters based on shape flags
- Handles both 8-bit and 16-bit color formats

## Key Types
- ConvertClass (Class): Manages palette conversion and blitting operations
- Blitter (Class): Base class for blitting operations (external)
- RLEBlitter (Class): Base class for RLE-aware blitting operations (external)
- ShapeFlags_Type (Enum): Flags defining rendering effects (external)

## Key Functions
### ConvertClass::ConvertClass
- Purpose: Initializes conversion tables and blitter objects based on palette and surface format
- Calls: W3DNEW, W3DNEWARRAY, HSVClass::Set_Value, PaletteClass::Closest_Color, DSurface::Build_Remap_Table, DSurface::Get_Halfbright_Mask, DSurface::Get_Quarterbright_Mask

### ConvertClass::~ConvertClass
- Purpose: Cleans up dynamically allocated blitter objects and tables
- Calls: delete, delete[]

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
- BlitPlainXlat, BlitTransXlat, BlitTransZRemapXlat, BlitTransRemapDest, BlitTransRemapXlat, BlitTransLucent75, BlitTransLucent50, BlitTransLucent25 (external)
- RLEBlitTransXlat, RLEBlitTransZRemapXlat, RLEBlitTransRemapDest, RLEBlitTransRemapXlat, RLEBlitTransLucent75, RLEBlitTransLucent50, RLEBlitTransLucent25 (external)
- PaletteClass, HSVClass, DSurface (external)
- W3DNEW, W3DNEWARRAY (memory allocation macros)
