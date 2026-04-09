# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FireOCLAfterWeaponCooldownUpdate.cpp

## Purpose
Manages firing of Object Creation Lists (OCL) after a weapon cooldown period, tracking weapon usage and upgrade conditions.

## Responsibilities
- Tracks weapon firing state and cooldowns
- Validates upgrade conditions for OCL creation
- Calculates OCL lifetime based on firing duration
- Creates OCLs when conditions are met

## Key Types
- `FireOCLAfterWeaponCooldownUpdateModuleData` (Class): Stores module configuration (weapon slot, OCL, shot requirements)
- `FireOCLAfterWeaponCooldownUpdate` (Class): Main update module handling weapon cooldown logic

## Key Functions
### `update`
- Purpose: Main update loop checking weapon state and firing conditions
- Calls: `getCurrentWeapon`, `getWeaponInWeaponSlot`, `getLastShotFrame`, `getPossibleNextShotFrame`, `fireOCL`, `resetStats`

### `fireOCL`
- Purpose: Creates OCL with calculated lifetime based on firing duration
- Calls: `ObjectCreationList::create`, `resetStats`

### `resetStats`
- Purpose: Resets tracking variables for consecutive shots and start frame

## Globals
- `TheGameLogic` (GameLogic*): Access to game logic system

## Dependencies
- `Common/Player.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `GameClient/Drawable.h`, `GameClient/InGameUI.h`
- `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/ObjectCreationList.h`, `GameLogic/Weapon.h`, `GameLogic/Weaponset.h`
- `GameLogic/Module/FireOCLAfterWeaponCooldownUpdate.h`, `GameLogic/Module/LifetimeUpdate.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/BodyModule.h`
