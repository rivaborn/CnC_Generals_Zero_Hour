# Generals/Code/Tools/WW3D/pluglib/realcrc.cpp

## Purpose
Implements CRC-32 checksum calculation functions for memory blocks and strings.

## Responsibilities
- Provides CRC-32 computation for memory buffers
- Provides CRC-32 computation for null-terminated strings
- Provides case-insensitive CRC-32 computation for strings
- Uses precomputed lookup table for efficient calculation

## Key Types
- None

## Key Functions
### CRC_Memory
- Purpose: Calculates CRC-32 for a block of memory
- Calls: CRC32 macro

### CRC_String
- Purpose: Calculates CRC-32 for a null-terminated string
- Calls: CRC32 macro

### CRC_Stringi
- Purpose: Calculates case-insensitive CRC-32 for a string
- Calls: CRC32 macro, toupper

## Globals
- CRC32_Table (unsigned long[256]): Precomputed CRC-32 lookup table

## Dependencies
- realcrc.h
- ctype.h (for toupper)
- CRC32 macro (defined in this file)
