# Generals/Code/Libraries/Source/WWVegas/WWLib/load.cpp

## Purpose
Handles data compression and decompression for file loading operations.

## Responsibilities
- Decompress data from compressed buffers
- Handle different compression methods (NOCOMPRESS, HORIZONTAL, LCW)
- Manage header interpretation for compressed data
- Support platform-specific byte ordering (AMIGA)

## Key Types
- `CompHeaderType` (struct): Contains compression metadata (size, skip, method)
- `CompressionType` (enum): Defines compression methods (NOCOMPRESS, HORIZONTAL, LCW)

## Key Functions
### `Uncompress_Data`
- Purpose: Decompresses data from source buffer to destination buffer
- Calls:
  - `Reverse_Long` (conditional)
  - `Reverse_Word` (conditional)
  - `LCW_Uncomp` (for LCW compression)
  - `memmove` (for NOCOMPRESS)

## Globals
None

## Dependencies
- `always.h`, `iff.h`, `lcw.h`, `string.h`
- `CompHeaderType`, `CompressionType` (external)
- `LCW_Uncomp` (external function)
- Platform-specific macros (`AMIGA`, `Reverse_Long`, `Reverse_Word`)
