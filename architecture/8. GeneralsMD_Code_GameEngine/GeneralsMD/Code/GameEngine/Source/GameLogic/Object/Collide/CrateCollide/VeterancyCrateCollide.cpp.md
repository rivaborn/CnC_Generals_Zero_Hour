# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/VeterancyCrateCollide.cpp

## Purpose
Handles collision logic for veterancy crates that grant experience levels to units.

## Responsibilities
- Determines valid targets for veterancy crate effects
- Applies experience gains to eligible units
- Manages special pilot veterancy behavior
- Serializes/deserializes crate state

## Key Types
- **VeterancyCrateCollide (Class)**: Manages veterancy crate collision behavior
- **VeterancyCrateCollideModuleData (Struct)**: Configuration data for veterancy crates

## Key Functions
### `getLevelsToGain`
- Purpose: Calculates experience levels to grant based on crate configuration
- Calls: `getVeterancyCrateCollideModuleData`, `getObject`, `getVeterancyLevel`

### `isValidToExecute`
- Purpose: Validates if a target unit can receive veterancy from this crate
- Calls: `getVeterancyCrateCollideModuleData`, `CrateCollide::isValidToExecute`, `isEffectivelyDead`, `isSignificantlyAboveTerrain`, `getExperienceTracker`, `isTrainable`, `canGainExpForLevel`, `getControllingPlayer`, `isUsingAirborneLocomotor`

### `executeCrateBehavior`
- Purpose: Applies veterancy effects to eligible units within range
- Calls: `getAIUpdateInterface`, `getGoalObject`, `getExperienceTracker`, `gainExpForLevel`, `ThePartitionManager->iterateObjectsInRange`, `TheScriptEngine->transferObjectName`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Serialization/deserialization handler
- Calls: `CrateCollide::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Object.h`, `GameLogic/PartitionManager.h`, `GameLogic/Module/VeterancyCrateCollide.h`, `GameLogic/ScriptEngine.h`, `GameLogic/Module/AIUpdate.h`
- `ThePartitionManager`, `TheScriptEngine`
