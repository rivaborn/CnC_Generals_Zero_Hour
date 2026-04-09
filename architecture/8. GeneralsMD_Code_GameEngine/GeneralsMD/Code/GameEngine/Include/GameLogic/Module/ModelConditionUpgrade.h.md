# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ModelConditionUpgrade.h

## Purpose
Defines a module for upgrading game objects by setting model condition flags.

## Responsibilities
- Declares `ModelConditionUpgradeModuleData` to store upgrade configuration.
- Defines `ModelConditionUpgrade` class to apply upgrades.
- Provides memory management macros for object pooling.
- Exposes module creation and data access macros.

## Key Types
- **ModelConditionFlagType (Enum)**: Type for model condition flags (purpose not inferable).
- **ModelConditionUpgradeModuleData (Class)**: Holds upgrade data including the flag type.
- **ModelConditionUpgrade (Class)**: Upgrade module that sets model condition flags on objects.
- **ModelConditionUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **ModelConditionUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### `ModelConditionUpgradeModuleData::buildFieldParse`
- Purpose: Parses module data from configuration files.
- Calls: Not inferable (likely uses `MultiIniFieldParse` methods).

### `ModelConditionUpgrade::upgradeImplementation`
- Purpose: Applies the upgrade by setting the model condition flag.
- Calls: Not inferable (likely interacts with `Thing` object).

### `ModelConditionUpgrade::isSubObjectsUpgrade`
- Purpose: Indicates whether the upgrade applies to sub-objects.
- Calls: None.

## Globals
- None.

## Dependencies
- `UpgradeModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `Thing` (game object being upgraded)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
