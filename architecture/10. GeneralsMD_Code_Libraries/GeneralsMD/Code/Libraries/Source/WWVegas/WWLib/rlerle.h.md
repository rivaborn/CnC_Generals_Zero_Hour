# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rlerle.h

## Purpose
Defines RLE (Run-Length Encoded) blitter classes for various pixel operations in the SAGE engine.

## Responsibilities
- Provides template-based RLE blitter classes for different pixel formats
- Handles transparency, translation, remapping, and blending operations
- Includes optimized assembly implementations for specific cases
- Manages pixel skipping for clipping purposes

## Key Types
- **RLEBlitTransXlat (Class)**: Basic RLE blitter with transparency and translation
- **RLEBlitTransRemapXlat (Class)**: RLE blitter with remapping and translation
- **RLEBlitTransZRemapXlat (Class)**: RLE blitter with double-indirected remapping
- **RLEBlitTransRemapDest (Class)**: RLE blitter that remaps destination pixels
- **RLEBlitTransDarken (Class)**: RLE blitter that darkens destination pixels
- **RLEBlitTransLucent50/25/75 (Class)**: RLE blitters for different translucency levels

## Key Functions
### Skip_Leading_Pixels
- Purpose: Skips leading pixels in RLE data for clipping
- Calls: None

### RLEBlitTransXlat::Blit
- Purpose: Blits RLE data with transparency and translation
- Calls: Skip_Leading_Pixels

### RLEBlitTransRemapXlat::Blit
- Purpose: Blits RLE data with remapping and translation
- Calls: Skip_Leading_Pixels

### RLEBlitTransZRemapXlat::Blit
- Purpose: Blits RLE data with double-indirected remapping
- Calls: Skip_Leading_Pixels

### RLEBlitTransRemapDest::Blit
- Purpose: Remaps destination pixels based on source transparency
- Calls: Skip_Leading_Pixels

### RLEBlitTransDarken::Blit
- Purpose: Darkens destination pixels where source is non-transparent
- Calls: Skip_Leading_Pixels

### RLEBlitTransLucent50/25/75::Blit
- Purpose: Blits with 50%, 25%, or 75% translucency respectively
- Calls: Skip_Leading_Pixels

## Globals
- None

## Dependencies
- blitter.h (RLEBlitter base class)
- <assert.h>
- <string.h>
