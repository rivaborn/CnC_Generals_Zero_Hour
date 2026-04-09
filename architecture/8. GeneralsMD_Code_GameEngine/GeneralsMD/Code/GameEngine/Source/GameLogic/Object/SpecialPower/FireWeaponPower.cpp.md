# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/FireWeaponPower.cpp

## Purpose
Implements a special power module that loads and fires a specific weapon controlled by a superweapon timer.

## Responsibilities
- Extends `SpecialPowerModule` to handle weapon firing logic
- Manages weapon reloading and AI targeting
- Supports firing at positions, objects, or default behavior
- Handles serialization (Xfer) and CRC for save/load

## Key Types
- `FireWeaponPowerModuleData` (Class): Stores module configuration (e.g., max shots)
- `FireWeaponPower` (Class): Main implementation of the fire weapon power

## Key Functions
### `FireWeaponPowerModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for module data
- Calls: `SpecialPowerModuleData::buildFieldParse`

### `FireWeaponPower::doSpecialPower`
- Purpose: Executes the special power with default targeting
- Calls: `SpecialPowerModule::doSpecialPower`, `getObject`, `getFireWeaponPowerModuleData`, `reloadAllAmmo`, `aiAttackPosition`, `setTurretTargetPosition`

### `FireWeaponPower::doSpecialPowerAtLocation`
- Purpose: Executes the special power targeting a specific location
- Calls: `SpecialPowerModule::doSpecialPowerAtLocation`, `getObject`, `getFireWeaponPowerModuleData`, `reloadAllAmmo`, `aiAttackPosition`, `setTurretTargetPosition`

### `FireWeaponPower::doSpecialPowerAtObject`
- Purpose: Executes the special power targeting a specific object
- Calls: `SpecialPowerModule::doSpecialPowerAtObject`, `getObject`, `getFireWeaponPowerModuleData`, `reloadAllAmmo`, `aiAttackObject`, `setTurretTargetObject`

### `FireWeaponPower::crc`
- Purpose: Generates CRC checksum for save/load
- Calls: `SpecialPowerModule::crc`

### `FireWeaponPower::xfer`
- Purpose: Serializes/deserializes the module state
- Calls: `SpecialPowerModule::xfer`, `xferVersion`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/Xfer.h`
- `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/WeaponSet.h`
- `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/FireWeaponPower.h`
- `SpecialPowerModule`, `AIUpdateInterface`, `Xfer`, `MultiIniFieldParse`
