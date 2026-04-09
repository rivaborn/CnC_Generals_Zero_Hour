# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DeletionUpdate.h

## Purpose
Defines a game logic module that destroys an object after a specified lifetime.

## Responsibilities
- Manages object deletion based on frame count
- Parses lifetime configuration from INI files
- Calculates sleep delays for efficient updates

## Key Types
- **DeletionUpdateModuleData (Class)**: Holds min/max lifetime frame values and INI parsing logic
- **DeletionUpdate (Class)**: UpdateModule that counts down to object deletion
- **DeletionUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **DeletionUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### DeletionUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsers for lifetime values
- Calls: UpdateModuleData::buildFieldParse

### DeletionUpdate::setLifetimeRange
- Purpose: Sets the min/max frames before deletion
- Calls: Not inferable

### DeletionUpdate::update
- Purpose: Updates the deletion counter and destroys object when time expires
- Calls: calcSleepDelay

### DeletionUpdate::calcSleepDelay
- Purpose: Calculates how long to sleep before next update
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h
- MultiIniFieldParse, INI namespace (for INI parsing)
- Thing class (game object base)
- ModuleData class (base module data)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Standard module macros (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
