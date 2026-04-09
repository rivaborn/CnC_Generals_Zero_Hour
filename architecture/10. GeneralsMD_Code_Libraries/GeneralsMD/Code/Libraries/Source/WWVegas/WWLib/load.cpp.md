# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/load.cpp

## Purpose
Handles file loading and uncompression operations for the game engine.

## Responsibilities
- Uncompress data from compressed buffers
- Load and write data files
- Handle different compression methods (NOCOMPRESS, HORIZONTAL, LCW)

## Key Types
- `CompHeaderType` (struct): Contains compression metadata (size, skip, method)
- `CompressionType` (enum): Defines compression methods (NOCOMPRESS, HORIZONTAL, LCW)

## Key Functions
### `Uncompress_Data`
- Purpose: Uncompresses data from source buffer to destination buffer
- Calls: `LCW_Uncomp`, `memmove`

## Globals
- None

## Dependencies
- `always.h`, `iff.h`, `lcw.h`, `string.h`
- `LCW_Uncomp` (external function)
- `Reverse_Long`, `Reverse_Word` (conditional Amiga byte-order functions)
