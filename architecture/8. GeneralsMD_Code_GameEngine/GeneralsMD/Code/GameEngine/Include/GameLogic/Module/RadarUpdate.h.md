# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RadarUpdate.h

## Purpose
Defines the RadarUpdate module for managing radar functionality on objects in the game.

## Responsibilities
- Manages radar extension and activation states
- Handles radar update logic via the UpdateModule interface
- Provides configuration for radar extend time via module data
- Tracks radar build progress and completion

## Key Types
- **RadarUpdateModuleData (Class)**: Holds radar configuration (extend time)
- **RadarUpdate (Class)**: Implements radar update logic and state management
- **RadarUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **RadarUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### RadarUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsing for radar module data
- Calls: UpdateModuleData::buildFieldParse

### RadarUpdate::extendRadar
- Purpose: Initiates radar extension process
- Calls: Not inferable

### RadarUpdate::update
- Purpose: Handles periodic radar update logic
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (for INI parsing)
- INI namespace (for parsing utilities)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
