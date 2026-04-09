# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HeightDieUpdate.cpp

## Purpose
Implements an update module that destroys objects when they fall below a specified height above terrain or structures.

## Responsibilities
- Tracks object position and height relative to terrain/structures
- Triggers object destruction when height threshold is crossed
- Manages attached particle destruction at specified height
- Handles initial delay before activation

## Key Types
- **HeightDieUpdateModuleData (struct)**: Stores configuration for height-based destruction (target height, flags, etc.)
- **HeightDieUpdate (class)**: Update module that enforces height-based destruction logic

## Key Functions
### `update`
- Purpose: Checks object height and triggers destruction if below threshold
- Calls: `TheTerrainLogic->getGroundHeight`, `ThePartitionManager->iterateObjectsInRange`, `getObject()->kill`, `TheParticleSystemManager->destroyAttachedSystems`

### `xfer`
- Purpose: Serializes module state for network synchronization
- Calls: `UpdateModule::xfer`, `xfer->xferBool`, `xfer->xferCoord3D`, `xfer->xferUnsignedInt`

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `ThingTemplate.h`, `Xfer.h`, `GameLogic.h`, `TerrainLogic.h`, `PartitionManager.h`
- `ContainModule.h`, `PhysicsUpdate.h`
- `ParticleSys.h` (for particle destruction)
