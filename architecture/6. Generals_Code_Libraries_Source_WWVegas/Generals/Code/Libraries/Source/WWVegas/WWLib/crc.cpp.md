# Generals/Code/Libraries/Source/WWVegas/WWLib/crc.cpp

## Purpose
Implements CRC (Cyclic Redundancy Check) computation for data integrity verification.

## Responsibilities
- Provides CRC calculation for byte/block data
- Manages staging buffer for efficient processing
- Supports string and memory CRC computation
- Uses precomputed lookup table for CRC32

## Key Types
- CRCEngine (Class): CRC computation engine with staging buffer
- CRC (Class): Static CRC utilities (Memory/String)

## Key Functions
### CRCEngine::operator()(char)
- Purpose: Processes a single byte through the CRC engine
- Calls: Value()

### CRCEngine::operator()(void const*, int)
- Purpose: Processes a data block of arbitrary length
- Calls: operator()(char), _lrotl, Value()

### CRC::Memory(unsigned char*, unsigned long, unsigned long)
- Purpose: Computes CRC for a memory block
- Calls: CRC32()

### CRC::String(const char*, unsigned long)
- Purpose: Computes CRC for a null-terminated string
- Calls: CRC32()

## Globals
- _Table[256] (unsigned long[]): Precomputed CRC32 lookup table

## Dependencies
- "always.h", "crc.h"
- _lrotl (intrinsic function)
