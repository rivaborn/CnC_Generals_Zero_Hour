# Generals/Code/Libraries/Source/WWVegas/WWLib/realcrc.cpp

## Purpose
Implements CRC-32 checksum calculation functions for memory blocks and strings.

## Responsibilities
- Provides CRC-32 calculation for memory blocks
- Provides CRC-32 calculation for NULL-terminated strings
- Provides case-insensitive CRC-32 calculation for strings
- Uses precomputed CRC lookup table for efficiency

## Key Types
- None

## Key Functions
### CRC_Memory
- Purpose: Calculates CRC-32 for a block of memory
- Calls: CRC32 macro

### CRC_String
- Purpose: Calculates CRC-32 for a NULL-terminated string
- Calls: CRC32 macro

### CRC_Stringi
- Purpose: Calculates case-insensitive CRC-32 for a string
- Calls: CRC32 macro, toupper

## Globals
- CRC32_Table (unsigned long[256]): Precomputed CRC lookup table for polynomial 0x04C11DB7

## Dependencies
- realcrc.h
- ctype.h (for toupper)
- CRC32 macro (defined in this file)
