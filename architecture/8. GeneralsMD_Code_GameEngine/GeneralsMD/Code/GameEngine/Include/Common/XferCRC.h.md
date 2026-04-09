# GeneralsMD/Code/GameEngine/Include/Common/XferCRC.h

## Purpose
Defines the XferCRC class for computing CRC checksums during data transfer operations.

## Responsibilities
- Computes CRC checksums for data blocks
- Implements Xfer interface methods for CRC calculation
- Manages CRC session lifecycle (open/close)
- Handles snapshot transfer with CRC computation

## Key Types
- **XferCRC (Class)**: CRC computation implementation for Xfer interface
- **Snapshot (Class)**: Forward reference to snapshot data structure

## Key Functions
### XferCRC::open
- Purpose: Starts a CRC session with the given identifier
- Calls: Not inferable

### XferCRC::xferSnapshot
- Purpose: Entry point for transferring a snapshot while computing CRC
- Calls: Not inferable

### XferCRC::getCRC
- Purpose: Returns the computed CRC in network byte order
- Calls: Not inferable

### XferCRC::addCRC
- Purpose: CRC computation for a 4-byte block
- Calls: Not inferable

## Globals
- None

## Dependencies
- Key includes: "Common/Xfer.h"
- External symbols: Xfer (base class), Snapshot (forward reference)
