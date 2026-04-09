# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SmartBombTargetHomingUpdate.h

## Purpose
Defines a game logic module that adjusts a falling object's trajectory to improve target homing accuracy.

## Responsibilities
- Adjusts object trajectory toward a target position
- Provides configuration for course correction strength
- Handles target position updates
- Implements update loop for trajectory correction

## Key Types
- **SmartBombTargetHomingUpdateModuleData (Class)**: Holds module configuration (course correction scalar)
- **SmartBombTargetHomingUpdate (Class)**: Implements the homing update logic
- **SmartBombTargetHomingUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **SmartBombTargetHomingUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### SmartBombTargetHomingUpdateModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: UpdateModuleData::buildFieldParse

### SmartBombTargetHomingUpdate::SetTargetPosition
- Purpose: Sets the target position for homing
- Calls: None visible

### SmartBombTargetHomingUpdate::update
- Purpose: Performs trajectory correction during game update
- Calls: None visible

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (for INI parsing)
- INI namespace (for parsing utilities)
- Coord3D (3D coordinate type)
- Thing (game entity base class)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
