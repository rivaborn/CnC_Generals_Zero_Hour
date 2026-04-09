# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ArmorUpgrade.h

## Purpose
Defines the `ArmorUpgrade` module class for handling armor upgrades in the game.

## Responsibilities
- Inherits from `UpgradeModule` to provide armor-specific upgrade functionality
- Manages armor upgrade logic via `upgradeImplementation`
- Determines if upgrade applies to sub-objects via `isSubObjectsUpgrade`
- Uses memory pool allocation for performance

## Key Types
- **ArmorUpgrade (Class)**: Armor upgrade module handling game object armor improvements
- **Thing (Class)**: Forward-declared reference to game objects being upgraded
- **ArmorUpgradeMagicEnum (Enum)**: Not inferable (line reference mismatch)
- **ArmorUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (line reference mismatch)

## Key Functions
### ArmorUpgrade::upgradeImplementation
- Purpose: Implements the core armor upgrade logic
- Calls: Not inferable (implementation not shown)

### ArmorUpgrade::isSubObjectsUpgrade
- Purpose: Determines if upgrade applies to sub-objects
- Calls: None

### ArmorUpgrade constructor
- Purpose: Initializes armor upgrade module for a specific Thing
- Calls: Parent `UpgradeModule` constructor

## Globals
None

## Dependencies
- `UpgradeModule.h` (parent class)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macros (`MAKE_STANDARD_MODULE_MACRO`)
- `Thing` class (forward reference)
