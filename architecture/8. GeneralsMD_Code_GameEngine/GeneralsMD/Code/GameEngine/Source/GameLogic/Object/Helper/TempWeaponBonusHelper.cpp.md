# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/TempWeaponBonusHelper.cpp

## Purpose
Manages temporary weapon bonus effects for game objects, including application and removal.

## Responsibilities
- Applies and clears temporary weapon bonuses
- Handles visual effects (tinting) for bonuses
- Manages timing for bonus expiration
- Serializes bonus state for save/load

## Key Types
- `TempWeaponBonusHelper` (Class): Helper for managing temporary weapon bonuses
- `WeaponBonusConditionType` (Enum): Type of weapon bonus condition

## Key Functions
### `update()`
- Purpose: Handles bonus expiration when timer elapses
- Calls: `clearTempWeaponBonus()`

### `clearTempWeaponBonus()`
- Purpose: Removes current weapon bonus and associated visual effects
- Calls: `getObject()->clearWeaponBonusCondition()`, `getDrawable()->clearTintStatus()`

### `doTempWeaponBonus()`
- Purpose: Applies a weapon bonus with specified duration
- Calls: `clearTempWeaponBonus()`, `getObject()->setWeaponBonusCondition()`, `getDrawable()->setTintStatus()`

### `xfer()`
- Purpose: Serializes bonus state for save/load
- Calls: `ObjectHelper::xfer()`

## Globals
- `TheGameLogic` (GameLogic*): Access to game logic system

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Module/TempWeaponBonusHelper.h`
- `GameClient/Drawable.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Weapon.h`
