# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UnpauseSpecialPowerUpgrade.h

## Purpose
Defines an upgrade module that starts the timer on a special power, enabling logic-side dependency on upgrades.

## Responsibilities
- Manages special power timer activation via upgrades
- Provides module data structure for configuration
- Implements upgrade behavior through `upgradeImplementation`
- Handles memory management via SAGE engine macros

## Key Types
- **SpecialPowerTemplate (Class)**: Reference to special power template
- **UnpauseSpecialPowerUpgradeModuleData (Class)**: Module data containing special power reference
- **UnpauseSpecialPowerUpgrade (Class)**: Main upgrade module class
- **UnpauseSpecialPowerUpgradeMagicEnum (Enum)**: Not inferable (likely internal SAGE enum)
- **UnpauseSpecialPowerUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal SAGE enum)

## Key Functions
### UnpauseSpecialPowerUpgradeModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

### UnpauseSpecialPowerUpgrade::upgradeImplementation
- Purpose: Implements the actual upgrade behavior (starts special power timer)
- Calls: Not inferable

### UnpauseSpecialPowerUpgrade::isSubObjectsUpgrade
- Purpose: Indicates this upgrade doesn't affect sub-objects
- Calls: None

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `SpecialPowerTemplate` (forward reference)
- SAGE engine macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
- `MultiIniFieldParse` (for configuration parsing)
