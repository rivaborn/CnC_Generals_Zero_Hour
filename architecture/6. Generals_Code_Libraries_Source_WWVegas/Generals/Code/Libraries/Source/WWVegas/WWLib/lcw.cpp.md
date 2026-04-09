# Generals/Code/Libraries/Source/WWVegas/WWLib/lcw.cpp

## Purpose
Implements LCW (Lempel-Ziv-Welch variant) compression and decompression for data blocks.

## Responsibilities
- Decompress LCW-encoded data using specific command codes
- Compress data using LCW algorithm (Windows-only)
- Handle various compression codes (short/medium/long runs and copies)
- Manage memory pointers and byte/word operations during compression/decompression

## Key Types
- None

## Key Functions
### LCW_Uncomp
- Purpose: Decompress LCW-encoded data using command codes
- Calls: None (direct memory operations only)

### LCW_Comp
- Purpose: Compress data using LCW algorithm (Windows-only via inline assembly)
- Calls: None (uses inline assembly for compression logic)

## Globals
- None

## Dependencies
- Key includes: "always.h", "lcw.h"
- External symbols: None
- Platform-specific: Uses inline assembly for Windows (_MSC_VER)
