# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/GhostObject.cpp

## Purpose
Manages ghost objects and their serialization in the game engine.

## Responsibilities
- Defines `GhostObject` and `GhostObjectManager` classes
- Handles object serialization/deserialization via `Xfer`
- Manages parent-child relationships between objects
- Provides CRC (checksum) functionality for objects

## Key Types
- `GhostObject` (Class): Base class for ghost objects with parent tracking
- `GhostObjectManager` (Class): Manages collection of ghost objects
- `GeometryType` (Type): Used for parent geometry type (external)

## Key Functions
### `GhostObject::xfer`
- Purpose: Serializes/deserializes ghost object data
- Calls: `xferVersion`, `xferObjectID`, `xferUser`, `xferBool`, `xferReal`, `xferCoord3D`, `TheGameLogic->findObjectByID`

### `GhostObjectManager::xfer`
- Purpose: Serializes/deserializes ghost object manager state
- Calls: `xferVersion`, `xferInt`

## Globals
- `TheGhostObjectManager` (GhostObjectManager*): Singleton instance of ghost object manager

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/GhostObject.h`, `GameLogic/Object.h`
- `Xfer`, `ObjectID`, `Object`, `PartitionData`, `INI_INVALID_DATA` (external)
