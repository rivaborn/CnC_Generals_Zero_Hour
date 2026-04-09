# GeneralsMD/Code/GameEngine/Include/Common/Snapshot.h

## Purpose
Defines the base class interface for data structures involved in game saves, loads, and CRC checks.

## Responsibilities
- Provides virtual methods for CRC, save/load, and post-processing
- Serves as the foundation for snapshot-capable game objects
- Supports serialization and integrity verification

## Key Types
- **Snapshot (Class)**: Base interface for snapshot-capable objects
- **Xfer (Class)**: Forward-declared transfer object (not defined here)

## Key Functions
### Snapshot()
- Purpose: Constructor for Snapshot.
- Calls: None

### ~Snapshot()
- Purpose: Destructor for Snapshot.
- Calls: None

### crc(Xfer *xfer)
- Purpose: Virtual method for running a "light" CRC check.
- Calls: None

### xfer(Xfer *xfer)
- Purpose: Virtual method for save/load/deep CRC operations.
- Calls: None

### loadPostProcess()
- Purpose: Virtual method for post-processing after loading.
- Calls: None

## Globals
- None

## Dependencies
- **Common/AsciiString.h**: Included for string handling
- **Xfer**: Forward-declared class used for data transfer
- **GameState, XferLoad, XferSave, XferCRC**: Friend classes with access to protected methods
