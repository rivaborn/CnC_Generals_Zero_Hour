# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireWeaponWhenDamagedBehavior.h

## Purpose
Defines a game logic module that triggers weapon fire when an object is damaged.

## Responsibilities
- Fires weapons in response to damage events
- Manages continuous weapon firing based on damage state
- Handles upgrade activation for weapon behavior
- Processes damage type filtering and thresholds

## Key Types
- **FireWeaponWhenDamagedBehaviorModuleData (Class)**: Configuration data for the behavior module
- **FireWeaponWhenDamagedBehavior (Class)**: Main behavior module that implements damage reaction logic
- **FireWeaponWhenDamagedBehaviorMagicEnum (Enum)**: Not inferable (likely internal enum)
- **FireWeaponWhenDamagedBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal enum)

## Key Functions
### FireWeaponWhenDamagedBehaviorModuleData::buildFieldParse
- Purpose: Defines INI field parsing for module configuration
- Calls: UpdateModuleData::buildFieldParse, UpgradeMuxData::getFieldParse

### FireWeaponWhenDamagedBehavior::onDamage
- Purpose: Handles damage events and triggers weapon fire
- Calls: Not visible in header

### FireWeaponWhenDamagedBehavior::update
- Purpose: Updates continuous weapon firing based on damage state
- Calls: Not visible in header

### FireWeaponWhenDamagedBehavior::upgradeImplementation
- Purpose: Implements upgrade behavior for the module
- Calls: setWakeFrame

## Globals
None

## Dependencies
- BehaviorModule.h
- UpgradeModule.h
- UpdateModule.h
- DamageModule.h
- Weapon.h
- MultiIniFieldParse
- INI parsing utilities
- Memory pool and module macro systems
