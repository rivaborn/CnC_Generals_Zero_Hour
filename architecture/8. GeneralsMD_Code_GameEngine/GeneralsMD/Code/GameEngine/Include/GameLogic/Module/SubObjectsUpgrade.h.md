# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SubObjectsUpgrade.h

## Purpose
Defines a module for showing/hiding subobjects based on upgrade status, overriding animation states.

## Responsibilities
- Manage subobject visibility via upgrade states
- Parse configuration data for show/hide subobjects
- Implement upgrade logic for subobject toggling

## Key Types
- **Thing (Class)**: Base object type this module attaches to
- **SubObjectsUpgradeModuleData (Class)**: Holds show/hide subobject name lists
- **SubObjectsUpgrade (Class)**: Module implementing subobject upgrade logic
- **SubObjectsUpgradeMagicEnum (Enum)**: Not inferable
- **SubObjectsUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### SubObjectsUpgradeModuleData::buildFieldParse
- Purpose: Parse configuration data for subobject names
- Calls: Not inferable

### SubObjectsUpgrade::upgradeImplementation
- Purpose: Core logic for toggling subobject visibility
- Calls: Not inferable

### SubObjectsUpgrade::isSubObjectsUpgrade
- Purpose: Identifies this as a subobject upgrade module
- Calls: None

## Globals
- None

## Dependencies
- `UpgradeModule.h`
- `MultiIniFieldParse`
- `AsciiString`
- `UpgradeModuleData`
- `UpgradeModule`
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
