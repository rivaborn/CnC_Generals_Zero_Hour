# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FireWeaponUpdate.cpp

## Purpose
Handles automatic weapon firing for game objects, managing delays and weapon readiness.

## Responsibilities
- Manages weapon allocation and firing
- Handles initial delay before first shot
- Checks if firing is allowed (weapon ready, not under construction, etc.)
- Serializes/deserializes weapon state

## Key Types
- **FireWeaponUpdateModuleData (Class)**: Stores weapon template and delay settings
- **FireWeaponUpdate (Class)**: Implements weapon firing logic

## Key Functions
### FireWeaponUpdate::update
- Purpose: Updates weapon firing state and fires if conditions are met
- Calls: `isOkayToFire`, `TheGameLogic->getFrame`, `m_weapon->forceFireWeapon`

### FireWeaponUpdate::isOkayToFire
- Purpose: Determines if weapon can fire based on status and delays
- Calls: `getObject`, `m_weapon->getStatus`, `TheGameLogic->getFrame`, `getObject()->getLastShotFiredFrame`

### FireWeaponUpdate::xfer
- Purpose: Serializes weapon state for network sync
- Calls: `UpdateModule::xfer`, `xfer->xferSnapshot`, `xfer->xferUnsignedInt`

## Globals
- **TheWeaponStore (External)**: Used to allocate weapons
- **TheGameLogic (External)**: Used for frame timing

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/FireWeaponUpdate.h`, `GameLogic/WeaponStatus.h`, `GameLogic/GameLogic.h`
