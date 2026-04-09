# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DynamicShroudClearingRangeUpdate.cpp

## Purpose
Manages dynamic shroud clearing range updates for game objects, including visual effects and state transitions.

## Responsibilities
- Controls shroud clearing range expansion/shrinkage over time
- Manages grid decal visual effects
- Handles state transitions (shrinking, sustaining, growing)
- Updates object vision range based on timers
- Cleans up resources when done

## Key Types
- **DynamicShroudClearingRangeUpdateModuleData (Class)**: Stores configuration for shroud clearing updates
- **DynamicShroudClearingRangeUpdate (Class)**: Main update module implementing the logic
- **DSCRUState (Enum)**: State machine states (NOT_STARTED_YET, SHRINKING, SUSTAINING, GROWING, DONE_FOREVER, SLEEPING)

## Key Functions
### DynamicShroudClearingRangeUpdate::update
- Purpose: Main update loop handling state transitions and vision range changes
- Calls: createGridDecals, animateGridDecals, killGridDecals, getObject, getDynamicShroudClearingRangeUpdateModuleData, TheGameLogic->getFrame

### DynamicShroudClearingRangeUpdate::createGridDecals
- Purpose: Creates visual decal effects around the object
- Calls: RadiusDecalTemplate::createRadiusDecal

### DynamicShroudClearingRangeUpdate::animateGridDecals
- Purpose: Updates decal positions and opacity based on current vision range
- Calls: getObject, getPosition

### DynamicShroudClearingRangeUpdate::killGridDecals
- Purpose: Cleans up all grid decal effects
- Calls: None

## Globals
- **GRID_FX_DECAL_COUNT (const int)**: Number of decals in the grid effect

## Dependencies
- Common/Xfer.h
- GameLogic/GameLogic.h
- GameLogic/Object.h
- GameLogic/Module/DynamicShroudClearingRangeUpdate.h
- PreRTS.h
- RadiusDecalTemplate (external class)
- UpdateModule (base class)
- MultiIniFieldParse (for INI parsing)
- INI parsing utilities
