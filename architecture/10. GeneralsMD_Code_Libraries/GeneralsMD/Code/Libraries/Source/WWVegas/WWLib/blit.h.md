# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blit.h

## Purpose
Header file declaring blitting (bit-block transfer) functions for surface manipulation in the SAGE engine.

## Responsibilities
- Declares functions for blitting between surfaces
- Provides RLE (Run-Length Encoded) blitting functions
- Declares buffer conversion functions for surfaces
- Defines interfaces for clipping rectangle-based blits

## Key Types
None

## Key Functions
### Bit_Blit
- Purpose: Performs a bit-block transfer between surfaces with clipping rectangles
- Calls: Not inferable

### RLE_Blit
- Purpose: Performs RLE-compressed blitting between surfaces with clipping rectangles
- Calls: Not inferable

### Buffer_Size
- Purpose: Calculates required buffer size for a surface region
- Calls: Not inferable

### To_Buffer
- Purpose: Converts a surface region to a buffer
- Calls: Not inferable

### From_Buffer
- Purpose: Converts a buffer back to a surface region
- Calls: Not inferable

## Globals
None

## Dependencies
- `blitter.h`: Blitter class definitions
- `buff.h`: Buffer class definitions
- `trect.h`: Rect class definitions
- `surface.h`: Surface class definitions
