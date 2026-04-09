# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/UnitCrateCollide.cpp

## Purpose
Handles collision logic for crates that spawn units when picked up.

## Responsibilities
- Spawns specified units when crate is collected
- Plays sound effect on crate pickup
- Manages position finding for spawned units

## Key Types
- **UnitCrateCollide (Class)**: Handles unit-spawning crate behavior
- **UnitCrateCollideModuleData (Not shown)**: Contains unit type and count data

## Key Functions
### `UnitCrateCollide::executeCrateBehavior`
- Purpose: Spawns units when crate is collected
- Calls: `getUnitCrateCollideModuleData`, `TheThingFactory->findTemplate`, `TheThingFactory->newObject`, `ThePartitionManager->findPositionAround`, `TheAudio->addAudioEvent`

### `UnitCrateCollide::crc`
- Purpose: Serialization CRC calculation
- Calls: `CrateCollide::crc`

### `UnitCrateCollide::xfer`
- Purpose: Serialization/deserialization
- Calls: `CrateCollide::xfer`

### `UnitCrateCollide::loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- **TheThingFactory (ThingFactory)**: Global object factory
- **ThePartitionManager (PartitionManager)**: Spatial partitioning system
- **TheAudio (Audio)**: Audio system interface

## Dependencies
- `PreRTS.h`, `Common/AudioEventRTS.h`, `Common/MiscAudio.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/PartitionManager.h`, `GameLogic/
