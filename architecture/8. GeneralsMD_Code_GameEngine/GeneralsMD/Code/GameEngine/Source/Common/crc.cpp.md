# GeneralsMD/Code/GameEngine/Source/Common/crc.cpp

## Purpose
Implements CRC (Cyclic Redundancy Check) computation for data integrity verification in debug builds.

## Responsibilities
- Computes CRC checksums for byte buffers
- Provides CRC value retrieval
- Handles bitwise CRC calculation logic

## Key Types
- None

## Key Functions
### `addCRC(UnsignedByte val)`
- Purpose: Updates CRC value with a single byte
- Calls: None

### `computeCRC(const void *buf, Int len)`
- Purpose: Computes CRC for a buffer of data
- Calls: `addCRC()`

### `get()`
- Purpose: Retrieves the current CRC value
- Calls: None

## Globals
- None

## Dependencies
- `Common/CRC.h` (header)
- `Common/Debug.h` (header)
- `PreRTS.h` (included first)
- `UnsignedByte`, `UnsignedInt`, `Int` (types)
- `_DEBUG` (preprocessor symbol)
