# Generals/Code/GameEngine/Source/GameLogic/Object/Update/HordeUpdate.cpp

## Purpose
Handles horde logic for game objects, including joining or leaving hordes and updating visual effects.

## Responsibilities
- Manage object's participation in hordes.
- Update visual effects based on horde status.
- Handle AI morale bonuses when entering or leaving a horde.

## Key Types
- **PartitionFilterHordeMember (Class)**: Filters objects for horde membership checks.

## Key Functions
### getHUI
- Purpose: Retrieves the `HordeUpdateInterface` from an object's behavior modules.
- Calls: None

### PartitionFilterHordeMember::allow
- Purpose: Determines if another object can join the horde based on various criteria.
- Calls: 
  - `Object::getTemplate`
  - `Object::isKindOfMulti`
  - `Object::getRelationship`
  - `Object::isOffMap`

### HordeUpdateModuleData::HordeUpdateModuleData
- Purpose: Initializes horde update module data with default values.
- Calls: None

### HordeUpdateModuleData::buildFieldParse
- Purpose: Builds field parsing for horde update module data from INI files.
- Calls: 
  - `INI::parseDurationUnsignedInt`
  - `KindOfMaskType::parseFromINI`
  - `INI::parseInt`
  - `INI::parseReal`
  - `INI::parseBool`
  - `INI::parseIndexList`

### HordeUpdate::HordeUpdate
- Purpose: Constructs the horde update module.
- Calls: 
  - `getHordeUpdateModuleData`
  - `setWakeFrame`
  - `GameLogicRandomValue`

### HordeUpdate::joinOrLeaveHorde
- Purpose: Handles joining or leaving a horde and applies morale bonuses.
- Calls: 
  - `getObject`
  - `getHordeUpdateModuleData`
  - `evaluateMoraleBonus`

### HordeUpdate::showHideFlag
- Purpose: Shows or hides the flag sub-object based on horde status.
- Calls: 
  - `getObject`
  - `getDrawable`
  - `showSubObject`
  - `updateSubObjects`

### HordeUpdate::onDrawableBoundToObject
- Purpose: Handles drawable binding to the object, initially hiding the flag.
- Calls: 
  - `showHideFlag`

### HordeUpdate::update
- Purpose: Updates horde status and visual effects every frame.
- Calls: 
  - `getObject`
  - `getHordeUpdateModuleData`
  - `iterateObjectsInRange`
  - `setTerrainDecal`
  - `setTerrainDecalSize`
  - `setTerrainDecalFadeTarget`

## Globals
- **DEFAULT_UPDATE_RATE (Int)**: Default update rate for horde checks.

## Dependencies
- Key includes:
  - "Common
