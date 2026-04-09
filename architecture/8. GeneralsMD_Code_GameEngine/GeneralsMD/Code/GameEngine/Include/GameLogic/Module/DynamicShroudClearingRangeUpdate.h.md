# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DynamicShroudClearingRangeUpdate.h

## Purpose
Defines a module for dynamically adjusting an object's shroud-clearing (vision) range over time.

## Responsibilities
- Manages vision range growth/shrink transitions with configurable delays and rates
- Handles pseudo-wireframe decal effects for visual feedback
- Tracks state machine for vision range updates
- Integrates with the game's module system

## Key Types
- **DynamicShroudClearingRangeUpdateModuleData (Class)**: Configuration data for the module (timing, final vision, decal settings)
- **DynamicShroudClearingRangeUpdate (Class)**: Core module implementing vision range updates and decal management
- **DSCRU_STATE (Enum)**: State machine states (NOT_STARTED_YET, GROWING, SUSTAINING, SHRINKING, DONE_FOREVER, SLEEPING)

## Key Functions
### DynamicShroudClearingRangeUpdate::update
- Purpose: State machine handler for vision range updates
- Calls: Not inferable (implementation in .cpp)

### DynamicShroudClearingRangeUpdate::createGridDecals
- Purpose: Creates visual decal effects for vision range changes
- Calls: Not inferable

### DynamicShroudClearingRangeUpdate::animateGridDecals
- Purpose: Animates existing decal effects
- Calls: Not inferable

## Globals
- **GRID_FX_DECAL_COUNT (const)**: Maximum number of decal effects (30)

## Dependencies
- `UpdateModule.h` (base class)
- `RadiusDecal.h` (for visual effects)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Standard
