# GeneralsMD/Code/GameEngine/Source/GameLogic/System/CaveSystem.cpp

## Purpose
Manages cave systems and tunnel trackers on the map.

## Responsibilities
- Tracks tunnel connections between caves
- Manages registration/unregistration of caves
- Handles serialization/deserialization of cave data
- Validates tunnel connection switches

## Key Types
- CaveSystem (Class): Main system class managing cave/tunnel logic
- TunnelTracker (Class): Tracks connections between caves (external)

## Key Functions
### `canSwitchIndexToIndex`
- Purpose: Checks if tunnel connection switch between two cave indices is allowed
- Calls: `getContainCount()` on tunnel trackers

### `registerNewCave`
- Purpose: Creates or reuses a tunnel tracker for a cave index
- Calls: `newInstance()` for TunnelTracker

### `xfer`
- Purpose: Serializes/deserializes cave system state
- Calls: `xferVersion`, `xferUnsignedShort`, `xferSnapshot` on Xfer object

## Globals
- TheCaveSystem (CaveSystem*): Singleton instance of cave system

## Dependencies
- Common/GameState.h
- Common/TunnelTracker.h
- Common/Xfer.h
- GameLogic/CaveSystem.h
- PreRTS.h
