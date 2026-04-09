# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzo1x.h

## Purpose
Header file defining the public interface for the LZO1X compression algorithm, part of the LZO real-time data compression library.

## Responsibilities
- Declares compression and decompression function prototypes for LZO1X algorithm
- Defines memory requirements for compression/decompression operations
- Provides constants for memory allocation sizes

## Key Types
None

## Key Functions
### lzo1x_decompress
- Purpose: Fast decompression of LZO1X compressed data
- Calls: Not inferable

### lzo1x_decompress_x
- Purpose: Safe decompression with overrun testing
- Calls: Not inferable

### lzo1x_1_compress
- Purpose: Fast compression using LZO1X algorithm
- Calls: Not inferable

### lzo1x_999_compress
- Purpose: Better compression ratio at cost of more memory and time
- Calls: Not inferable

## Globals
- LZO1X_MEM_COMPRESS (lzo_uint): Memory required for compression
- LZO1X_MEM_DECOMPRESS (lzo_uint): Memory required for decompression (0)
- LZO1X_999_MEM_COMPRESS (lzo_uint): Memory required for 999 compression level

## Dependencies
- lzoconf.h: Configuration header for LZO library
- LZO_EXTERN: Macro for external function declaration (defined in lzoconf.h)
