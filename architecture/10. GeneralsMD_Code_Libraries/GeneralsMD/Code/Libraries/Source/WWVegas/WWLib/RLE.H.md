# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RLE.H

## Purpose
Defines the RLEEngine class for Run-Length Encoding (RLE) compression/decompression of data, optimized for runs of zero bytes.

## Responsibilities
- Provides RLE compression/decompression for arbitrary data blocks
- Supports line-based compression/decompression for sprite storage
- Handles zero-byte run-length encoding efficiently

## Key Types
- RLEEngine (Class): RLE compression/decompression engine for zero-byte runs

## Key Functions
### Compress
- Purpose: Compresses data using RLE for zero-byte runs
- Calls: Not inferable

### Decompress
- Purpose: Decompresses RLE-compressed data
- Calls: Not inferable

### Line_Compress
- Purpose: Compresses line-encoded data blocks (for sprites)
- Calls: Not inferable

### Line_Decompress
- Purpose: Decompresses line-encoded data blocks
- Calls: Not inferable

## Globals
- None

## Dependencies
- None (header-only, no external symbols)
