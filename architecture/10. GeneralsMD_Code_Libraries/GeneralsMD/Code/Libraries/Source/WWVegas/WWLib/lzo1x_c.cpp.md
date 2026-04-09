# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzo1x_c.cpp

## Purpose
Implements the LZO1X-1 data compression algorithm for the game engine.

## Responsibilities
- Compresses data blocks using LZO1X-1 algorithm
- Manages dictionary-based matching for compression
- Handles literal runs and match encoding
- Provides public entry point for compression

## Key Types
- None (procedural implementation)

## Key Functions
### do_compress
- Purpose: Core compression function that processes input data and generates compressed output
- Calls: UPDATE_D, UPDATE_I, LZO_CHECK_MPOS_NON_DET, assert

### lzo1x_1_compress
- Purpose: Public entry point for LZO1X-1 compression
- Calls: do_compress

## Globals
- None

## Dependencies
- "always.h", "lzo1x.h", "lzo_conf.h", "wwdebug.h", <assert.h>
- LZO_E_OK, LZO_BYTE, lzo_uint, lzo_voidp, lzo_bytepp, lzo_ptrdiff_t (from LZO library)
