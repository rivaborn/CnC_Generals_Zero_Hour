# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StatusBitsUpgrade.h

## Purpose
Defines a module for upgrading objects by modifying their status bits.

## Responsibilities
- Manages status bit upgrades for game objects
- Provides module data for status bit configuration
- Implements upgrade logic via `upgradeImplementation`
- Handles memory management for module instances

## Key Types
- **StatusBitsUpgradeModuleData (Class)**: Holds status bits to set/clear
- **StatusBitsUpgrade (Class)**: Implements the upgrade module behavior
- **StatusBitsUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro)
- **StatusBitsUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro)

## Key Functions
### StatusBitsUpgrade::upgradeImplementation
- Purpose: Executes the actual upgrade logic
- Calls: Not inferable (implementation in .cpp)

### StatusBitsUpgrade::isSubObjectsUpgrade
- Purpose: Indicates whether upgrade applies to sub-objects
- Calls: None

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `Common/ObjectStatusTypes.h` (status bit types)
- `Thing` (forward reference)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
