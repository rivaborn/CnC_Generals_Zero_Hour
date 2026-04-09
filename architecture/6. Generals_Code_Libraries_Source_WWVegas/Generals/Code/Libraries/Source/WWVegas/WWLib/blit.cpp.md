# Generals/Code/Libraries/Source/WWVegas/WWLib/blit.cpp

## Purpose
Provides pixel blitting operations for surface rendering, including regular and RLE-compressed data with clipping support.

## Responsibilities
- Perform pixel block transfers between surfaces
- Handle clipping for source/destination rectangles
- Support RLE-compressed sprite rendering
- Buffer size calculations and surface-to-buffer conversions

## Key Types
- `Surface` (Class): Base surface interface for pixel operations
- `Rect` (Struct): Rectangle definition for clipping/blitting regions
- `Blitter` (Class): Abstract pixel transfer operation handler
- `RLEBlitter` (Class): Specialized blitter for RLE-compressed data
- `Buffer` (Class): Linear memory buffer for pixel data storage

## Key Functions
### `Buffer_Size`
- Purpose: Calculate required buffer size for given surface dimensions
- Calls: `surface.Bytes_Per_Pixel()`

### `To_Buffer`
- Purpose: Copy surface region to linear memory buffer
- Calls: `BSurface` constructor, `Blit_From`

### `From_Buffer`
- Purpose: Copy buffer data to surface region
- Calls: `BSurface` constructor, `Blit_From`

### `Bit_Blit` (overload 1)
- Purpose: Dispatch blit with surface-level clipping
- Calls: `Bit_Blit` (overload 2)

### `Bit_Blit` (overload 2)
- Purpose: Perform clipped pixel block transfer
- Calls: `XSurface::Prep_For_Blit`, `blitter.BlitForward/BlitBackward`

### `RLE_Blit` (overload 1)
- Purpose: Dispatch RLE blit with surface-level clipping
- Calls: `RLE_Blit` (overload 2)

### `RLE_Blit` (overload 2)
- Purpose: Render RLE-compressed sprite with clipping
- Calls: `Blit_Clip`, `blitter.Blit`

## Globals
None

## Dependencies
- `always.h`, `blit.h`, `bsurface.h`, `xsurface.h`
- `Surface`, `Rect`, `Blitter`, `RLEBlitter`, `Buffer` classes
- `XSurface::Prep_For_Blit`, `Blit_Clip` functions
