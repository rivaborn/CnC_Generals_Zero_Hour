# Generals/Code/Libraries/Source/WWVegas/WWLib/rlerle.h

## Purpose
Defines RLE (Run-Length Encoded) blitter classes for rendering operations with various pixel manipulation effects.

## Responsibilities
- Provides templated blitter classes for RLE decompression with transparency
- Supports pixel translation, remapping, darkening, and translucency effects
- Includes optimized assembly implementations for specific pixel formats
- Handles clipping via leading pixel skipping

## Key Types
- **RLEBlitTransXlat (Class)**: Basic RLE blitter with pixel translation
- **RLEBlitTransRemapXlat (Class)**: RLE blitter with remap and translation
- **RLEBlitTransZRemapXlat (Class)**: RLE blitter with dynamic remap and translation
- **RLEBlitTransRemapDest (Class)**: RLE blitter that remaps destination pixels
- **RLEBlitTransDarken (Class)**: RLE blitter that darkens destination pixels
- **RLEBlitTransLucent50 (Class)**: RLE blitter with 50% translucency
- **RLEBlitTransLucent25 (Class)**: RLE blitter with 25% translucency
- **RLEBlitTransLucent75 (Class)**: RLE blitter with 75% translucency

## Key Functions
### Skip_Leading_Pixels
- Purpose: Skips transparent pixels in RLE stream for clipping
- Calls: None

### RLEBlitTransXlat::Blit
- Purpose: Decompresses RLE data with pixel translation
- Calls: Skip_Leading_Pixels

### RLEBlitTransRemapXlat::Blit
- Purpose: Decompresses RLE data with remap and translation
- Calls: Skip_Leading_Pixels

### RLEBlitTransZRemapXlat::Blit
- Purpose: Decompresses RLE data with dynamic remap and translation
- Calls: Skip_Leading_Pixels

### RLEBlitTransRemapDest::Blit
- Purpose: Remaps destination pixels based on source transparency
- Calls: Skip_Leading_Pixels

### RLEBlitTransDarken::Blit
- Purpose: Darkens destination pixels where source is opaque
- Calls: Skip_Leading_Pixels

### RLEBlitTransLucent50::Blit
- Purpose: Applies 50% translucency effect during blit
- Calls: Skip_Leading_Pixels

### RLEBlitTransLucent25::Blit
- Purpose: Applies 25% translucency effect during blit
- Calls: Skip_Leading_Pixels

### RLEBlitTransLucent75::Blit
- Purpose: Applies 75% translucency effect during blit
- Calls: Skip_Leading_Pixels

## Globals
None

## Dependencies
- blitter.h (RLEBlitter base class)
- <assert.h>
- <string.h>
