# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blit.cpp

## Purpose
Provides pixel blitting operations for surface rendering, including regular and RLE-compressed data transfer.

## Responsibilities
- Calculate buffer sizes for pixel data
- Transfer pixel data between surfaces and buffers
- Perform clipped blitting operations
- Handle RLE-compressed sprite rendering
- Manage surface locking/unlocking during transfers

## Key Types
- `Buffer` (struct): Linear RAM buffer for pixel data storage
- `Blitter` (class): Abstract base for pixel copying operations
- `RLEBlitter` (class): Specialized blitter for RLE-compressed data
- `Surface` (class): Surface rendering interface
- `Rect` (struct): Rectangle definition for clipping/blitting

## Key Functions
### `Buffer_Size`
- Purpose: Calculates required buffer size for given surface dimensions
- Calls: `surface.Bytes_Per_Pixel()`

### `To_Buffer`
- Purpose: Copies surface rectangle to linear buffer
- Calls: `rect.Is_Valid()`, `BSurface` constructor, `Blit_From`

### `From_Buffer`
- Purpose: Copies buffer data to surface rectangle
- Calls: `rect.Is_Valid()`, `BSurface` constructor, `Blit_From`

### `Bit_Blit` (overload 1)
- Purpose: Blits with surface-level clipping
- Calls: Overloaded `Bit_Blit`

### `Bit_Blit` (overload 2)
- Purpose: Performs clipped pixel blitting with stride handling
- Calls: `XSurface::Prep_For_Blit`, `blitter.BlitForward/BlitBackward`, `dest.Unlock`, `source.Unlock`

### `RLE_Blit` (overload 1)
- Purpose: RLE blitting with surface-level clipping
- Calls: Overloaded `RLE_Blit`

### `RLE_Blit` (overload 2)
- Purpose: Handles RLE-compressed sprite rendering with clipping
- Calls: `Blit_Clip`, `dest.Lock`, `source.Lock`, `blitter.Blit`, `dest.Unlock`, `source.Unlock`

## Globals
None

## Dependencies
- `always.h`, `blit.h`, `bsurface.h`, `xsurface.h`
- `Surface`, `Rect`, `Buffer`, `Blitter`, `RLEBlitter` classes
- `XSurface::Prep_For_Blit`, `Blit_Clip` functions
