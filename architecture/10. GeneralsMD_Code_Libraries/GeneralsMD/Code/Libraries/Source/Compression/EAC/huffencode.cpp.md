# GeneralsMD/Code/Libraries/Source/Compression/EAC/huffencode.cpp

## Purpose
Implements Huffman encoding for data compression in the SAGE engine.

## Responsibilities
- Manages Huffman tree construction and bitstream encoding
- Handles delta encoding for input data
- Writes compressed bitstreams with headers
- Provides public API for compression (HUFF_encode)

## Key Types
- **HUFFMemStruct (struct)**: Tracks memory buffer pointer and length
- **HuffEncodeContext (struct)**: Main encoding context with bitstream, tree, and pattern data
- **None**: No classes/enums beyond these

## Key Functions
### HUFF_writebits
- Purpose: Writes a bit pattern to the output buffer
- Calls: HUFF_writebits (recursive)

### HUFF_maketree
- Purpose: Constructs Huffman tree from frequency counts
- Calls: HUFF_treechase

### HUFF_pack
- Purpose: Packs data using Huffman codes and writes headers
- Calls: HUFF_writenum, HUFF_writeexp, HUFF_writecode, HUFF_writebits

### HUFF_encode
- Purpose: Public API for compressing data
- Calls: HUFF_packfile, galloc, gfree

## Globals
- None

## Dependencies
- **Includes**: string.h, codex.h, huffcodex.h
- **External**: galloc, gfree (memory allocation), GCALL (calling convention)
