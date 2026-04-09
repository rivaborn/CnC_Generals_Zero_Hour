# GeneralsMD/Code/GameEngine/Include/Common/crc.h

## Purpose
Provides a CRC (Cyclic Redundancy Check) calculation class for data integrity verification.

## Responsibilities
- Encapsulates CRC computation logic
- Supports incremental CRC calculation
- Provports clearing and retrieving CRC values
- Provides optimized debug and release versions

## Key Types
- CRC (Class): Encapsulates CRC calculation functionality

## Key Functions
### CRC::computeCRC
- Purpose: Computes CRC for a buffer and adds it to the current CRC
- Calls: CRC::addCRC (debug only)

### CRC::clear
- Purpose: Resets the CRC value to 0
- Calls: None

### CRC::get
- Purpose: Returns the current CRC value
- Calls: None

## Globals
None

## Dependencies
- Lib/BaseType.h (for basic types)
- winsock2.h (for htonl)
- _asm (inline assembly in release build)
