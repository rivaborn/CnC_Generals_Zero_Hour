# GeneralsMD/Code/GameEngine/Source/Common/RTS/ActionManager.cpp

## Purpose
Centralizes logical queries about object actions in the game world, used for UI validation and network command processing.

## Responsibilities
- Validates action legality (repairs, docks, special powers)
- Handles shroud/fog-of-war checks for actions
- Manages special power targeting rules
- Provides weapon firing validation
- Supports garrisoning logic

## Key Types
- **ActionManager (Class)**: Core action validation system
- **CommandSourceType (Enum)**: Tracks action origin (player, script, etc.)
- **SpecialPowerType (Enum)**: Defines special ability types

## Key Functions
### `canGetRepairedAt`
- Purpose: Checks if object can be repaired at target location
- Calls: `isObjectShroudedForAction`, `getBodyModule`

### `canDoSpecialPower`
- Purpose: Validates special power usage eligibility
- Calls: `hasSpecialPower`, `getSpecialPowerModule`

### `canFireWeaponAtObject`
- Purpose: Determines if weapon can target specific object
- Calls: `getAbleToAttackSpecificObject`, `estimateWeaponDamage`

### `isObjectShroudedForAction`
- Purpose: Checks if target is obscured by fog-of-war
- Calls: `getShroudedStatus`

## Globals
- **TheActionManager (ActionManager*)**: Singleton instance

## Dependencies
- GameLogic modules (Object, Weapon, PartitionManager)
- Common game systems (Player, Team, SpecialPower)
- UI and client systems (InGameUI, Drawable)
