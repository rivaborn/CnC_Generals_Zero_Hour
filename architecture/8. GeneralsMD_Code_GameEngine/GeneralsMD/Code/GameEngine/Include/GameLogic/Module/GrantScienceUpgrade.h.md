# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GrantScienceUpgrade.h

## Purpose
Defines a module that grants a science upgrade when requirements are met.

## Responsibilities
- Inherits from `UpgradeModule` to provide science-granting functionality.
- Uses `GrantScienceUpgradeModuleData` to store configuration (e.g., science name).
- Implements `upgradeImplementation` to apply the science upgrade.
- Manages memory via `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`.

## Key Types
- **GrantScienceUpgradeModuleData (Class)**: Stores the science name to grant.
- **GrantScienceUpgrade (Class)**: Core module class handling science upgrades.
- **GrantScienceUpgradeMagicEnum (Enum)**: Not inferable (empty).
- **GrantScienceUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty).

## Key Functions
### `GrantScienceUpgrade::upgradeImplementation`
- Purpose: Applies the science upgrade logic.
- Calls: Not inferable (implementation in `.cpp`).

### `GrantScienceUpgrade::isSubObjectsUpgrade`
- Purpose: Indicates whether the upgrade applies to sub-objects.
- Calls: None.

## Globals
- None.

## Dependencies
- `UpgradeModule.h` (base class).
- `MultiIniFieldParse` (for parsing module data).
- `AsciiString`, `Thing`, `ModuleData`, `ScienceType` (external types).
