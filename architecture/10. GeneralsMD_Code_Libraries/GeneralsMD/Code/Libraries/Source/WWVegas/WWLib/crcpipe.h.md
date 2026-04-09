# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/crcpipe.h

## Purpose
Defines a `CRCPipe` class that computes a CRC checksum while piping data through.

## Responsibilities
- Inherits from `Pipe` to process data streams.
- Computes CRC checksum incrementally via `Put()`.
- Provides access to the final CRC result via `Result()`.
- Prevents copying via private copy constructor/assignment.

## Key Types
- **CRCPipe (Class)**: A pipe that calculates CRC checksums on passed data.

## Key Functions
### CRCPipe::Put
- Purpose: Processes data and updates the CRC checksum.
- Calls: `CRCEngine` methods (not inferable).

### CRCPipe::Result
- Purpose: Returns the computed CRC checksum.
- Calls: None.

## Globals
- None.

## Dependencies
- `crc.h` (for `CRCEngine`)
- `pipe.h` (base class `Pipe`)
