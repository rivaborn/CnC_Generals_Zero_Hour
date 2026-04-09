# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/WeaponBonusUpdate.cpp

## Purpose
Handles temporary weapon bonus application to objects within a range, including those inside transports.

## Responsibilities
- Applies weapon bonuses to eligible objects in range
- Filters objects based on kind requirements and restrictions
- Processes contained objects (e.g., inside transports)
- Manages update timing and module data parsing

## Key Types
- `tempWeaponBonusData` (struct): Temporary data container for bonus parameters passed during iteration

## Key Functions
### `containIteratingDoTempWeaponBonus`
- Purpose: Applies weapon bonus to contained objects (e.g., inside transports)
- Calls: `Object::doTempWeaponBonus`

### `WeaponBonusUpdate::update`
- Purpose: Main update loop that scans and applies bonuses
- Calls: `ThePartitionManager->iterateObjectsInRange`, `Object::doTempWeaponBonus`, `ContainModule::iterateContained`

## Globals
- None

## Dependencies
- `WeaponBonusUpdateModuleData` (from WeaponBonusUpdate.h)
- `UpdateModule` (base class)
- `Object`, `PartitionManager`, `ContainModule`, `Weapon`
- `MultiIniFieldParse`, `KindOfMaskType`, `INI` (for parsing)
- `Xfer` (for serialization)
