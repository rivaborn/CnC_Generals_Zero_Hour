# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/LockWeaponCreate.cpp

## Purpose
Handles locking a weapon slot for an object during its creation phase in the game.

## Responsibilities
- Initializes weapon slot locking data
- Parses configuration for which weapon slot to lock
- Applies permanent weapon lock on object build completion
- Manages serialization (Xfer) and CRC for network sync

## Key Types
- `LockWeaponCreateModuleData` (Class): Stores configuration for which weapon slot to lock
- `LockWeaponCreate` (Class): Module that enforces weapon slot locking on object creation

## Key Functions
### `LockWeaponCreateModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for weapon slot configuration
- Calls: `CreateModuleData::buildFieldParse`

### `LockWeaponCreate::onBuildComplete`
- Purpose: Applies permanent weapon lock to the object's specified slot
- Calls: `CreateModule::onBuildComplete`, `getObject`, `getLockWeaponCreateModuleData`

### `LockWeaponCreate::xfer`
- Purpose: Handles network serialization of the module
- Calls: `CreateModule::xfer`, `xfer->xferVersion`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Xfer.h`, `LockWeaponCreate.h`, `Object.h`, `WeaponSet.h`
- `INI` namespace, `MultiIniFieldParse`, `Xfer`, `Thing`, `ModuleData`, `Object`, `WeaponSlotType`
