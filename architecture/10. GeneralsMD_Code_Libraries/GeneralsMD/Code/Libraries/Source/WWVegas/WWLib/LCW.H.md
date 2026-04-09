# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/LCW.H

## Purpose
Header file declaring compression/decompression functions for the LCW (LZW-like) algorithm.

## Responsibilities
- Declares LCW compression and decompression functions
- Provides platform-specific conditional compilation
- Includes OS-dependent headers for Unix

## Key Types
- None

## Key Functions
### LCW_Uncomp
- Purpose: Decompresses data using LCW algorithm
- Calls: None

### LCW_Comp
- Purpose: Compresses data using LCW algorithm
- Calls: None

## Globals
- None

## Dependencies
- "osdep.h" (included conditionally for Unix)
- _MSC_VER (Microsoft compiler version check)
- _UNIX (platform detection macro)
