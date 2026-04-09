# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireWeaponUpdate.h

## Purpose
Defines a game logic module that makes a unit fire its weapon at its own position repeatedly.

## Responsibilities
- Manages weapon firing behavior for a unit
- Handles initial delay before firing starts
- Checks if it's safe to fire (e.g., weapon cooldown)
- Provides module data configuration for weapon templates and delays

## Key Types
- **FireWeaponUpdateModuleData (Class)**: Holds configuration data for the firing behavior (weapon template, delays)
- **FireWeaponUpdate (Class)**: Implements the update module that triggers weapon firing
- **FireWeaponUpdateMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **FireWeaponUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### FireWeaponUpdate::update
- Purpose: Handles the periodic firing logic for the weapon.
- Calls: `isOkayToFire()`

### FireWeaponUpdate::isOkayToFire
- Purpose: Determines if the weapon can be fired based on cooldown and exclusivity rules.
- Calls: Not inferable (implementation in .cpp file)

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `Weapon.h` (for weapon templates)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
