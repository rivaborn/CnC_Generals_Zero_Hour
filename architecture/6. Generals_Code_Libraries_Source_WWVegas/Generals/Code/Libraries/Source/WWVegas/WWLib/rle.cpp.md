# Generals/Code/Libraries/Source/WWVegas/WWLib/rle.cpp

## Purpose
Implements Run-Length Encoding (RLE) compression and decompression for byte sequences, used for optimizing data storage and transfer.

## Responsibilities
- Compresses byte sequences using RLE
- Decompresses RLE-compressed byte sequences
- Handles line-specific compression/decompression with length metadata
- Manages buffer pointers and lengths during compression/decompression

## Key Types
- RLEEngine (Class): Core class providing RLE compression/decompression functionality

## Key Functions
### RLEEngine::Compress
- Purpose: Compresses a sequence of bytes using RLE
- Calls: None (direct)

### RLEEngine::Line_Compress
- Purpose: Compresses a line of data and stores its length at the beginning of the output buffer
- Calls: Compress

### RLEEngine::Decompress
- Purpose: Decompresses a sequence of RLE-compressed bytes
- Calls: None (direct)

### RLEEngine::Line_Decompress
- Purpose: Decompresses a line-compressed RLE data sequence
- Calls: Decompress

## Globals
None

## Dependencies
- "always.h", "rle.h", <assert.h>, <stdlib.h>
- Uses MIN macro (from "always.h")
- External symbols: None
