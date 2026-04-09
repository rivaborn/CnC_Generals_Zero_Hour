# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/FireWeaponCollide.cpp

## Purpose
Handles weapon firing when objects collide, implementing the FireWeaponCollide module behavior.

## Responsibilities
- Manages weapon allocation and firing during collisions
- Evaluates collision conditions (status flags, fire-once behavior)
- Serializes module state for network synchronization
- Integrates with the game's collision and weapon systems

## Key Types
- **FireWeaponCollideModuleData (Class)**: Module configuration data (weapon template, status flags, fire-once setting)
- **FireWeaponCollide (Class)**: Collision-based weapon firing module implementation

## Key Functions
### `buildFieldParse`
- Purpose: Registers INI field parsers for module data
- Calls: `CollideModuleData::buildFieldParse`

### `onCollide`
- Purpose: Handles collision events and triggers weapon fire
- Calls: `shouldFireWeapon`, `m_collideWeapon->loadAmmoNow`, `m_collideWeapon->fireWeapon`

### `shouldFireWeapon`
- Purpose: Determines if weapon should fire based on object status and module settings
- Calls: `getObject()->getStatusBits`, `status.testForAll`, `status.testForAny`

### `xfer`
- Purpose: Serializes module state for network synchronization
- Calls: `CollideModule::xfer`, `xfer->xferSnapshot`

## Globals
- **TheWeaponStore (External)**: Weapon template allocation service

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/FireWeaponCollide.h`
- `INI`, `ObjectStatusMaskType`, `WeaponStore`, `Xfer`, `Coord3D`
