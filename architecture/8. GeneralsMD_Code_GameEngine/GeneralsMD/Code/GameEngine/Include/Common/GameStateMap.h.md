# GeneralsMD/Code/GameEngine/Include/Common/GameStateMap.h

## Purpose
Defines the `GameStateMap` class, which manages the pristine map state for save games in the SAGE engine.

## Responsibilities
- Manages map state serialization/deserialization via `Snapshot` interface
- Provides methods for CRC calculation and data transfer
- Handles scratch pad map cleanup
- Implements subsystem lifecycle methods (init/reset/update)

## Key Types
- **GameStateMap (Class)**: Manages pristine map state for save games
- **Xfer (Class)**: Forward-declared transfer object for serialization

## Key Functions
### `GameStateMap::xfer`
- Purpose: Handles data transfer for serialization/deserialization
- Calls: None (implementation not shown)

### `GameStateMap::clearScratchPadMaps`
- Purpose: Clears temporary scratch pad maps from the save directory
- Calls: None (implementation not shown)

## Globals
- **TheGameStateMap (GameStateMap*)**: Global instance of the map state manager

## Dependencies
- `Common/Snapshot.h`: Base class for serialization
- `Common/SubsystemInterface.h`: Subsystem lifecycle interface
- `Xfer` class (forward-declared): Used for data transfer operations
