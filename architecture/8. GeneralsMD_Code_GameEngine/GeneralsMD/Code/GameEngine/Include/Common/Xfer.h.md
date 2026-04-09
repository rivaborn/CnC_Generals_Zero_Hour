# GeneralsMD/Code/GameEngine/Include/Common/Xfer.h

## Purpose
Defines the Xfer system for serializing/deserializing game data, supporting save/load operations, CRC computation, and cross-subsystem data transfer.

## Responsibilities
- Declares enums for transfer modes, status codes, and options
- Defines the base Xfer class with virtual methods for data transfer
- Provides default implementations for common data types
- Manages transfer state (mode, options, identifier)

## Key Types
- **XferMode (Enum)**: Transfer operation type (save/load/CRC)
- **XferStatus (Enum)**: Status codes for transfer operations
- **XferOptions (Enum)**: Transfer behavior flags
- **Xfer (Class)**: Base class for data transfer operations

## Key Functions
### Xfer::xferImplementation
- Purpose: Abstract method for derived classes to implement actual data transfer
- Calls: None (pure virtual)

### Xfer::xferSnapshot
- Purpose: Entry point for transferring game snapshots
- Calls: None (pure virtual)

### Xfer::xferUser
- Purpose: Transfers arbitrary binary data
- Calls: xferImplementation

## Globals
- **XferVersion (Type)**: Version identifier for transfer format

## Dependencies
- Common/STLTypedefs.h
- Common/ModelState.h
- Common/Science.h
- Common/Upgrade.h
- Forward references: Snapshot, Matrix3D, and various enum types
