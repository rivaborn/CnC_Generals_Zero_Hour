# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzo1x_d.cpp

## Purpose
Implements the LZO1X decompression algorithm for the game engine.

## Responsibilities
- Decompresses LZO1X-compressed data blocks
- Handles literal runs and match references
- Manages decompression state and error conditions
- Calculates output length

## Key Types
- None

## Key Functions
### lzo1x_decompress
- Purpose: Decompresses LZO1X-compressed data into output buffer
- Calls: assert (via assert.h)

## Globals
- None

## Dependencies
- "always.h"
- "lzo1x.h"
- assert.h
- LZO_E_OK, LZO_E_ERROR, LZO_E_EOF_NOT_FOUND (error codes)
- lzo_byte, lzo_uint, lzo_voidp (LZO types)
