# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzo.h

## Purpose
Header file defining LZO compression/decompression functionality and wrapper class.

## Responsibilities
- Declares LZO compression/decompression functions
- Provides C++ wrapper class for LZO operations
- Defines buffer size calculations for LZO operations

## Key Types
- LZOCompressor (Class): Wrapper for LZO compression/decompression with work buffer management

## Key Functions
### lzo1x_1_compress
- Purpose: Compress data using LZO algorithm
- Calls: None (external LZO implementation)

### lzo1x_decompress
- Purpose: Decompress LZO-compressed data
- Calls: None (external LZO implementation)

### LZOCompressor::Compress
- Purpose: Static wrapper for LZO compression
- Calls: lzo1x_1_compress

### LZOCompressor::Decompress
- Purpose: Static wrapper for LZO decompression
- Calls: lzo1x_decompress

## Globals
- LZOCompressor::WorkBuffer (lzo_byte[]): Internal work buffer for compression
- LZOCompressor::EOWorkBuffer (lzo_byte*): End of work buffer marker

## Dependencies
- lzoconf.h
- lzo1x.h
- External LZO implementation functions
