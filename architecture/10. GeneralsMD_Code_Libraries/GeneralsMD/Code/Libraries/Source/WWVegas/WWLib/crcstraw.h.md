# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crcstraw.h

## Purpose
Declares the `CRCStraw` class, a `Straw` subclass that computes a CRC checksum from data passed through it.

## Responsibilities
- Inherits from `Straw` to process data streams.
- Computes CRC checksum incrementally as data flows through.
- Provides access to the final CRC result.
- Prevents copying via private copy constructor and assignment operator.

## Key Types
- **CRCStraw (Class)**: A `Straw` that calculates CRC checksums on data passed through it.

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
