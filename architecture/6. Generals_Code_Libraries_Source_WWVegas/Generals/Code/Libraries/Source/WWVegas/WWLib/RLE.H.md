# Generals/Code/Libraries/Source/WWVegas/WWLib/RLE.H

## Purpose
Provides RLE (Run-Length Encoding) compression/decompression for data blocks, optimized for runs of zero bytes.

## Responsibilities
- Compress/decompress arbitrary data blocks
- Handle line-based compression for sprite storage
- Support zero-byte run-length encoding

## Key Types
- RLEEngine (Class): RLE compression/decompression engine

## Key Functions
### Compress
- Purpose: Compress data using RLE for zero-byte runs
- Calls: Not inferable

### Decompress
- Purpose: Decompress RLE-compressed data
- Calls: Not inferable

### Line_Compress
- Purpose: Compress data with length encoding for sprite storage
- Calls: Not inferable

### Line_Decompress
- Purpose: Decompress length-encoded sprite data
- Calls: Not inferable

## Globals
- None

## Dependencies
- None (header-only)
