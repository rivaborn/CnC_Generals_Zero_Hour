# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RadiusDecalUpdate.h

## Purpose
Defines a game module for managing radius decals (visual effects) on game objects.

## Responsibilities
- Manages creation and destruction of radius decals
- Handles decal updates during game logic ticks
- Provides configuration via module data
- Supports conditional decal removal when objects stop attacking

## Key Types
- **RadiusDecalUpdateModuleData (Class)**: Module data container with field parsing
- **RadiusDecalUpdate (Class)**: Main module class handling decal lifecycle
- **RadiusDecalUpdateMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **RadiusDecalUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### RadiusDecalUpdateModuleData::buildFieldParse
- Purpose: Registers module data fields for INI parsing
- Calls: UpdateModuleData::buildFieldParse

### RadiusDecalUpdate::createRadiusDecal
- Purpose: Creates a new radius decal at specified position
- Calls: Not inferable (implementation in .cpp)

### RadiusDecalUpdate::update
- Purpose: Updates decal state during game logic tick
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- RadiusDecal.h (decal implementation)
- MultiIniFieldParse (INI parsing)
- Memory pool and module macro utilities
