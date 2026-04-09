# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/CRC.H

## Purpose
Provides CRC (Cyclic Redundancy Check) calculation functionality for data integrity verification.

## Responsibilities
- Implements a CRC engine class for incremental CRC computation
- Provides static CRC functions for block memory and string CRC calculation
- Supports both method-style and operator-style CRC computation

## Key Types
- CRCEngine (Class): Incremental CRC computation engine
- CRC (Class): Static CRC calculation utilities
- _Table (Array): Precomputed CRC lookup table

## Key Functions
### CRCEngine::operator()(char datum)
- Purpose: Adds a single byte to the CRC accumulator
- Calls: None

### CRCEngine::operator()(void const * buffer, int length)
- Purpose: Processes a buffer of data into the CRC
- Calls: None

### CRC::Memory(unsigned char *data, unsigned long length, unsigned long crc)
- Purpose: Computes CRC for a block of memory
- Calls: CRC32 macro

### CRC::String(const char *string, unsigned long crc)
- Purpose: Computes CRC for a null-terminated string
- Calls: CRC32 macro

## Globals
- _Table (unsigned long[256]): Precomputed CRC lookup table

## Dependencies
- stdlib.h
- osdep.h (on UNIX)
- _lrotl intrinsic function
