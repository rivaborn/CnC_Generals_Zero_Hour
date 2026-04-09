# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/ConvertToCarBombCrateCollide.cpp

## Purpose
Handles collision logic for converting units into car bombs when interacting with a special crate.

## Responsibilities
- Validates if a unit can be converted into a car bomb
- Executes the conversion process (applying effects, changing ownership, etc.)
- Manages serialization and network synchronization

## Key Types
- **ConvertToCarBombCrateCollide (Class)**: Handles car bomb conversion crate collision behavior
- **ModuleData (Type)**: Configuration data for the module

## Key Functions
### `isValidToExecute`
- Purpose: Checks if a unit is eligible for car bomb conversion
- Calls: `CrateCollide::isValidToExecute`, `other->isEffectivelyDead`, `other->isKindOf`, `other->getStatusBits`, `other->getTemplate->findWeaponTemplateSet`, `other->testWeaponSetFlag`

### `executeCrateBehavior`
- Purpose: Performs the car bomb conversion on a valid unit
- Calls: `getObject->getAIUpdateInterface->getGoalObject`, `other->checkAndDetonateBoobyTrap`, `other->setWeaponSetFlag`, `FXList::doFXObj`, `other->defect`, `TheScriptEngine->transferObjectName`, `other->setVisionRange`, `other->setShroudClearingRange`, `other->setStatus`, `other->getExperienceTracker->setVeterancyLevel`, `TheRadar->removeObject`, `TheRadar->addObject`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `CrateCollide::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- **TheRadar (Radar)**: Global radar system
- **TheScriptEngine (ScriptEngine)**: Global script engine

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Radar.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `GameClient/FXList.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Object.h`, `GameLogic/Module/ConvertToCarBombCrateCollide.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/ScriptEngine.h`
