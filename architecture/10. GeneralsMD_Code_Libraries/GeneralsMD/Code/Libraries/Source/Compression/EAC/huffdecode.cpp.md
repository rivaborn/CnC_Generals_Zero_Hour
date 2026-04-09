# GeneralsMD/Code/Libraries/Source/Compression/EAC/huffdecode.cpp

## Purpose
Implements Huffman decompression for the game's compression system.

## Responsibilities
- Decompresses Huffman-encoded data
- Validates compressed data headers
- Calculates uncompressed data size
- Handles delta and accelerated encoding modes

## Key Types
- **HuffDecodeContext (Class)**: Tracks decompression state (source pointer, bit buffer, bit count)
- **None**: No other classes/structs/enums defined

## Key Functions
### HUFF_decompress
- Purpose: Decompresses Huffman-encoded data into output buffer
- Calls: SQgetbits, SQgetnum, SQmemset, GET16BITS

### HUFF_is
- Purpose: Checks if data is valid Huffman-compressed data
- Calls: ggetm

### HUFF_size
- Purpose: Returns uncompressed size from compressed data header
- Calls: ggetm

### HUFF_decode
- Purpose: Wrapper for HUFF_decompress
- Calls: HUFF_decompress

## Globals
- **ZERO (int)**: Constant zero value used in bit manipulation

## Dependencies
- Key includes: `string.h`, `codex.h`, `huffcodex.h`
- External symbols: `ggetm`, `GCALL` (calling convention macro)
