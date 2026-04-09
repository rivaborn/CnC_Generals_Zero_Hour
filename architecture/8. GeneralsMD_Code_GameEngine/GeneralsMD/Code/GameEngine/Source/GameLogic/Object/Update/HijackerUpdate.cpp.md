# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HijackerUpdate.cpp

## Purpose
Manages the behavior of a hijacker unit when it hijacks a vehicle, including position tracking and state transitions.

## Responsibilities
- Tracks hijacker position relative to hijacked vehicle
- Handles vehicle destruction and hijacker ejection
- Manages hijacker visibility and collision state
- Transfers experience between hijacker and vehicle
- Spawns parachute if vehicle was airborne

## Key Types
- **HijackerUpdate (class)**: Manages hijacker vehicle interaction logic
- **HijackerUpdateModuleData (struct)**: Contains module configuration (not shown in file)

## Key Functions
### `update`
- Purpose: Updates hijacker position and state based on vehicle status
- Calls: `getObject`, `getTargetObject`, `setPosition`, `getExperienceTracker`, `setVeterancyLevel`, `ThePartitionManager->registerObject`, `getDrawable`, `setDrawableHidden`, `clearStatus`, `getAIUpdateInterface`, `aiIdle`, `TheThingFactory->findTemplate`, `newObject`, `getContain`, `isValidContainerFor`, `addToContain`

### `setTargetObject`
- Purpose: Sets the target vehicle for hijacking
- Calls: `getID`, `findObjectByID`

### `getTargetObject`
- Purpose: Retrieves the currently hijacked vehicle
- Calls: `findObjectByID`

### `crc`
- Purpose: Serialization checksum calculation
- Calls: `UpdateModule::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `UpdateModule::xfer`, `xferVersion`, `xferObjectID`, `xferCoord3D`, `xferBool`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `UpdateModule::loadPostProcess`, `findObjectByID`, `setTargetObject`

## Globals
- **ThePartitionManager**: Partition manager instance
- **TheThingFactory**: Thing factory instance
- **TheGameLogic**: Game logic instance

## Dependencies
- Common/Player.h, Common/ThingFactory.h, Common/ThingTemplate.h, Common/Xfer.h
- GameClient/Drawable.h, GameLogic/Object.h, GameLogic/Module/HijackerUpdate.h
- GameLogic/Module/AIUpdate.h, GameLogic/GameLogic.h, GameLogic/PartitionManager.h
- GameLogic/Module/EjectPilotDie.h, GameLogic/Module/ContainModule.h
- GameLogic/ExperienceTracker.h
