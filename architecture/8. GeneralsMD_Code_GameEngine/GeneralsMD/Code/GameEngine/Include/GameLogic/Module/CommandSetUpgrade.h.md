# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CommandSetUpgrade.h

## Purpose
Defines a module for upgrading command sets in the game, allowing dynamic replacement of command set strings.

## Responsibilities
- Manages command set upgrade data (primary/alternate command sets and trigger)
- Provides module infrastructure for command set upgrades
- Implements upgrade logic for command sets
- Handles memory management via memory pool macros

## Key Types
- **CommandSetUpgradeModuleData (Class)**: Stores upgrade configuration (new command sets and trigger)
- **CommandSetUpgrade (Class)**: Implements the upgrade module behavior
- **CommandSetUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **CommandSetUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### CommandSetUpgradeModuleData::buildFieldParse
- Purpose: Parses configuration data from ini files
- Calls: Not inferable (likely MultiIniFieldParse methods)

### CommandSetUpgrade::upgradeImplementation
- Purpose: Executes the actual command set upgrade logic
- Calls: Not inferable

### CommandSetUpgrade::isSubObjectsUpgrade
- Purpose: Indicates whether this upgrade affects sub-objects
- Calls: None

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `AsciiString` (string handling)
- `MultiIniFieldParse` (configuration parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
