# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RadarUpgrade.h

## Purpose
Defines the radar upgrade module for objects in the game, allowing them to provide radar functionality.

## Responsibilities
- Manages radar upgrade behavior for objects
- Handles radar upgrade data and module lifecycle
- Implements upgrade-specific logic (enable/disable radar)
- Supports team changes and object deletion

## Key Types
- **RadarUpgradeModuleData (Class)**: Stores radar upgrade configuration (disable-proof flag)
- **RadarUpgrade (Class)**: Implements radar upgrade functionality for objects
- **RadarUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **RadarUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### RadarUpgradeModuleData::buildFieldParse
- Purpose: Parses configuration data for radar upgrades
- Calls: Not inferable

### RadarUpgrade::onDelete
- Purpose: Cleans up when the radar upgrade is removed
- Calls: Not inferable

### RadarUpgrade::onCapture
- Purpose: Handles team changes for objects with radar upgrades
- Calls: Not inferable

### RadarUpgrade::upgradeImplementation
- Purpose: Implements the core radar upgrade logic
- Calls: Not inferable

### RadarUpgrade::isSubObjectsUpgrade
- Purpose: Determines if sub-objects should be upgraded
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `Thing` (forward reference)
- `Player` (forward reference)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
