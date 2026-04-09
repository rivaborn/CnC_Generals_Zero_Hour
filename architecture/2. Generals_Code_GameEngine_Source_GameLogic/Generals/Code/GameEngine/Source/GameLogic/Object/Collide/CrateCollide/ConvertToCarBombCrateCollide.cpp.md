# Generals/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/ConvertToCarBombCrateCollide.cpp

## Purpose
This file implements the `ConvertToCarBombCrateCollide` class, which handles the behavior of a crate that converts nearby vehicles into car bombs.

## Responsibilities
- Validate if an object can be converted to a car bomb.
- Execute the conversion process by modifying the target vehicle's properties.
- Handle serialization and deserialization of the module data.

## Key Types
- `ConvertToCarBombCrateCollide` (Class): Manages the conversion of vehicles into car bombs.

## Key Functions
### isValidToExecute
- Purpose: Determines if a given object can be converted to a car bomb.
- Calls:
  - `CrateCollide::isValidToExecute`
  - `other->isEffectivelyDead`
  - `other->isKindOf`
  - `other->getStatusBits`
  - `other->getTemplate()->findWeaponTemplateSet`
  - `set->testWeaponSetFlag`
  - `other->testWeaponSetFlag`

### executeCrateBehavior
- Purpose: Converts the target vehicle into a car bomb by setting relevant flags and properties.
- Calls:
  - `getObject()->getAIUpdateInterface()->getGoalObject`
  - `other->setWeaponSetFlag`
  - `FXList::doFXObj`
  - `other->defect`
  - `TheScriptEngine->transferObjectName`
  - `other->setVisionRange`
  - `other->setShroudClearingRange`
  - `other->setStatus`
  - `exp->setVeterancyLevel`
  - `TheRadar->removeObject`
  - `TheRadar->addObject`

### crc
- Purpose: Handles CRC serialization for the module data.
- Calls:
  - `CrateCollide::crc`

### xfer
