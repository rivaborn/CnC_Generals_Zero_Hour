# Generals/Code/Libraries/Source/WWVegas/WWLib/crcstraw.h

## Purpose
Header file defining a `CRCStraw` class for computing CRC checksums from data streams.

## Responsibilities
- Inherits from `Straw` to process data streams.
- Computes CRC values incrementally as data passes through.
- Provides access to the final CRC result.
- Prevents copying via private copy constructor and assignment operator.

## Key Types
- **CRCStraw (Class)**: A `Straw` subclass that calculates CRC checksums from data streams.

## Key Functions
### CRCStraw::Get
- Purpose: Processes data and updates the CRC checksum.
- Calls: `CRCEngine` methods (not visible in header).

### CRCStraw::Result
- Purpose: Returns the computed CRC value.
- Calls: None.

## Globals
- None.

## Dependencies
- `crc.h` (for `CRCEngine`)
- `straw.h` (base class `Straw`)
