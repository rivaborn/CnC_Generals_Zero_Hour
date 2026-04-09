# GeneralsMD/Code/Libraries/Source/Compression/EAC/huffcodex.h

## Purpose
Header file for Huffman compression/decompression functions in the EAC codex library.

## Responsibilities
- Declares Huffman codec API functions
- Defines macros for min/max operations
- Ensures proper include order (codex.h must be included first)

## Key Types
- CODEXABOUT (struct): Not inferable (likely contains codec metadata)
- None (other types)

## Key Functions
### HUFF_about
- Purpose: Returns codec information
- Calls: None

### HUFF_is
- Purpose: Checks if data is Huffman compressed
- Calls: None

### HUFF_size
- Purpose: Returns decompressed size from compressed data
- Calls: None

### HUFF_decode
- Purpose: Decompresses Huffman-encoded data
- Calls: None

### HUFF_encode
- Purpose: Compresses data using Huffman encoding
- Calls: None

## Globals
- None

## Dependencies
- codex.h (must be included before this file)
- GCALL macro (calling convention)
- bool type
