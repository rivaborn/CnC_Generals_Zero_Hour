# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/MobNexusContain.cpp

## Purpose
Handles containment logic for "MobNexus" units (e.g., transport vehicles) in the game.

## Responsibilities
- Manages loading/unloading of units into/from transport vehicles
- Handles special exit behaviors (scattering, orientation, velocity inheritance)
- Implements health regeneration for contained units
- Validates containment based on relationships and capacity
- Manages initial payloads and slot accounting

## Key Types
- **MobNexusContainModuleData (struct)**: Contains configuration for MobNexus behavior (slots, exit settings, health regen)
- **MobNexusContain (class)**: Implements the containment module for transport vehicles

## Key Functions
### `isValidContainerFor`
- Purpose: Checks if a unit can be contained and if there's capacity
- Calls: `OpenContain::isValidContainerFor`, `getRelationship`, `getTransportSlotCount`

### `onContaining`
- Purpose: Handles logic when a unit is loaded into the transport
- Calls: `OpenContain::onContaining`, `setDisabled`, `setModelConditionState`

### `onRemoving`
- Purpose: Handles logic when a unit is unloaded from the transport
- Calls: `OpenContain::onRemoving`, `clearDisabled`, `getPristineBonePositions`, `convertBonePosToWorldPos`, `setPosition`, `setOrientation`, `applyMotiveForce`, `setPitchRate`, `scatterToNearbyPosition`

### `update`
- Purpose: Updates health regeneration for contained units
- Calls: `getContainedItemsList`, `getBodyModule`, `getMaxHealth`, `attemptHealing`

### `reserveDoorForExit`
- Purpose: Determines if a unit can exit the transport
- Calls: `getAiFreeToExit`, `isUsingAirborneLocomotor`, `validMovementTerrain`

### `tryToEvacuate`
- Purpose: Attempts to unload all contained units
- Calls: `reserveDoorForExit`, `exitObjectViaDoor`, `getStealth`, `markAsDetected`

## Globals
- **None**

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/ThingTemplate.h`, `Common/ThingFactory.h`, `Common/Xfer.h`
- `GameClient/Drawable.h`, `GameLogic/AI.h`, `GameLogic/AIPathfind.h`, `GameLogic/Locomotor.h`
- `GameLogic/Module/StealthUpdate.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/BodyModule.h`
- `GameLogic/Module/MobNexus
