# Generals/Code/Libraries/Source/WWVegas/WWLib/crcpipe.h

## Purpose
Defines a `CRCPipe` class that computes a CRC checksum while piping data through.

## Responsibilities
- Inherits from `Pipe` to process data streams.
- Computes CRC checksums incrementally via `Put()`.
- Provides access to the final CRC result via `Result()`.
- Prevents copying via private copy constructor/assignment.

## Key Types
- **CRCPipe (Class)**: A pipe that computes CRC checksums on passed data.

## Key Functions
### CRCPipe::Put
- Purpose: Feeds data into the CRC engine.
- Calls: `CRCEngine` methods (not inferable).

### CRCPipe::Result
- Purpose: Returns the computed CRC value.
- Calls: None.

## Globals
- None.

## Dependencies
- `crc.h` (for `CRCEngine`)
- `pipe.h` (base class `Pipe`)
