# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lcw.cpp

## Purpose
Implements LCW (Lempel-Ziv-Welch variant) compression and decompression for the game engine.

## Responsibilities
- Provides `LCW_Uncomp` for decompressing LCW-encoded data
- Provides `LCW_Comp` for compressing data using LCW algorithm
- Handles various compression codes (short/medium/long runs and copies)
- Manages memory pointers and byte/word operations during compression/decompression

## Key Types
- None

## Key Functions
### LCW_Uncomp
- Purpose: Decompresses LCW-encoded data using specified command codes
- Calls: None (direct memory operations only)

### LCW_Comp
- Purpose: Compresses data using LCW algorithm with multiple run/copy strategies
- Calls: None (uses inline assembly for compression logic)

## Globals
- None

## Dependencies
- Key includes: "always.h", "lcw.h"
- External symbols: None
- Platform-specific: Uses `_MSC_VER` and `_WINDOWS` for assembly implementation
