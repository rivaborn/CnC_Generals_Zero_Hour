# Generals/Code/Libraries/Source/WWVegas/WWLib/realcrc.h

## Purpose
Header file declaring CRC (cyclic redundancy check) computation functions for memory blocks and strings.

## Responsibilities
- Declares CRC calculation functions for data integrity checks
- Provides both case-sensitive and case-insensitive string CRC variants
- Supports incremental CRC computation via default parameter

## Key Types
None

## Key Functions
### CRC_Memory
- Purpose: Computes CRC for a block of memory
- Calls: Not inferable

### CRC_String
- Purpose: Computes CRC for a null-terminated string (case-sensitive)
- Calls: Not inferable

### CRC_Stringi
- Purpose: Computes CRC for a null-terminated string (case-insensitive)
- Calls: Not inferable

## Globals
None

## Dependencies
- Standard C types (unsigned long, unsigned char, char)
- No external symbols used
