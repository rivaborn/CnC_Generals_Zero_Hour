# Generals/Code/Libraries/Source/WWVegas/WWLib/blit.h

## Purpose
Header file declaring blitting operations for surface rendering in the SAGE engine.

## Responsibilities
- Declares bit blit and RLE blit functions for surface rendering
- Provides buffer serialization functions for surfaces
- Defines interfaces for blitter and RLE blitter classes

## Key Types
- `Surface` (Class): Surface rendering target/source
- `Rect` (Struct): Rectangle region definition
- `Blitter` (Class): Base blitter interface
- `RLEBlitter` (Class): Run-length encoded blitter interface
- `Buffer` (Class): Serialization buffer

## Key Functions
### `Bit_Blit`
- Purpose: Performs bit-level blitting between surfaces
- Calls: Not inferable (implementation in .cpp)

### `RLE_Blit`
- Purpose: Performs RLE-encoded blitting between surfaces
- Calls: Not inferable (implementation in .cpp)

### `Buffer_Size`
- Purpose: Calculates buffer size required for surface serialization
- Calls: Not inferable

### `To_Buffer`
- Purpose: Serializes surface region to buffer
- Calls: Not inferable

### `From_Buffer`
- Purpose: Deserializes buffer to surface region
- Calls: Not inferable

## Globals
None

## Dependencies
- `blitter.h`: Blitter interface definitions
- `buff.h`: Buffer class definitions
- `trect.h`: Rectangle definitions
- `surface.h`: Surface class definitions
