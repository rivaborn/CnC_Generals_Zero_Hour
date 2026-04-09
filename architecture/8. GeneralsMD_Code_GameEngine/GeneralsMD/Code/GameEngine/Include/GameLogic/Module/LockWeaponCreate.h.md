# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/LockWeaponCreate.h

## Purpose
Defines a game module that locks a weapon slot during object creation.

## Responsibilities
- Locks weapon choice to a specified slot on object creation
- Provides module data structure for configuration
- Implements standard module lifecycle methods

## Key Types
- **LockWeaponCreateModuleData (Class)**: Holds configuration data for weapon slot locking
- **LockWeaponCreate (Class)**: Main module class that implements weapon locking behavior
- **LockWeaponCreateMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **LockWeaponCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### LockWeaponCreateModuleData::buildFieldParse
- Purpose: Parses configuration data from game files
- Calls: Not inferable

### LockWeaponCreate::onCreate
- Purpose: Handles weapon slot locking during object creation
- Calls: Not inferable

### LockWeaponCreate::onBuildComplete
- Purpose: Called when object creation is finished
- Calls: Not inferable

## Globals
None

## Dependencies
- `CreateModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `Thing` (game object base class)
- `WeaponSlotType` (weapon slot enumeration)
- Standard module macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
