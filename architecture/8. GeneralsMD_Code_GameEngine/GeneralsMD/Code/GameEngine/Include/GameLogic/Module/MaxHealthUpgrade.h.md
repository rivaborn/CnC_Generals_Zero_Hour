# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MaxHealthUpgrade.h

## Purpose
Defines a module for upgrading an object's maximum health in the game.

## Responsibilities
- Provides data structure for max health upgrade configuration
- Implements the upgrade logic for increasing object health
- Manages module creation and memory allocation
- Handles upgrade implementation and sub-object upgrade behavior

## Key Types
- **Thing (Class)**: Base object class being upgraded
- **MaxHealthChangeType (Enum)**: Type of max health change (not defined here)
- **MaxHealthUpgradeModuleData (Class)**: Holds upgrade configuration data
- **MaxHealthUpgrade (Class)**: Implements the health upgrade module
- **MaxHealthUpgradeMagicEnum (Enum)**: Module magic enum (not defined here)

## Key Functions
### MaxHealthUpgradeModuleData::buildFieldParse
- Purpose: Parses configuration data from ini files
- Calls: Not inferable

### MaxHealthUpgrade::upgradeImplementation
- Purpose: Contains the core logic for applying health upgrades
- Calls: Not inferable

### MaxHealthUpgrade::isSubObjectsUpgrade
- Purpose: Determines if upgrade applies to sub-objects
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpgradeModule.h (base class)
- MultiIniFieldParse (for configuration parsing)
- Memory pool and module macro utilities (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE, MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
