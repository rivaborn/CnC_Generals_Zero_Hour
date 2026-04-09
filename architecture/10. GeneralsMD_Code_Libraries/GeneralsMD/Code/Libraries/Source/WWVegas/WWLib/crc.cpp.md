# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crc.cpp

## Purpose
Implements CRC (Cyclic Redundancy Check) computation for data integrity verification.

## Responsibilities
- Provides CRC calculation for byte and block data
- Manages staging buffer for efficient processing
- Supports both incremental and bulk CRC computation
- Includes precomputed CRC table for polynomial 0x04C11DB7

## Key Types
- CRCEngine (Class): CRC computation engine with staging buffer
- CRC (Class): Static CRC utilities (Memory, String functions)

## Key Functions
### CRCEngine::operator()(char)
- Purpose: Processes a single byte of data through the CRC engine
- Calls: Value()

### CRCEngine::operator()(void const*, int)
- Purpose: Processes a block of data through the CRC engine
- Calls: operator()(char), Value(), _lrotl

### CRC::Memory(unsigned char*, unsigned long, unsigned long)
- Purpose: Computes CRC for a memory block
- Calls: CRC32()

### CRC::String(const char*, unsigned long)
- Purpose: Computes CRC for a null-terminated string
- Calls: CRC32()

## Globals
- _Table[256] (unsigned long[]): Precomputed CRC lookup table

## Dependencies
- "always.h", "crc.h"
- _lrotl (intrinsic function)
