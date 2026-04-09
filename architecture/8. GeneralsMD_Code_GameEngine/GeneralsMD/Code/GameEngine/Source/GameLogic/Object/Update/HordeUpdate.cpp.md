# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HordeUpdate.cpp

## Purpose
Manages horde behavior for game objects, including group detection, morale bonuses, and visual effects like terrain decals.

## Responsibilities
- Detects when objects are in a horde (group) based on proximity and configuration
- Applies morale bonuses when in a horde
- Manages visual effects (terrain decals) for horde members
- Handles horde membership state transitions

## Key Types
- **PartitionFilterHordeMember (Class)**: Filters objects to determine horde membership eligibility
- **HordeUpdateModuleData (Class)**: Configuration data for horde behavior (not fully shown in symbols)
- **HordeUpdate (Class)**: Main horde update module handling group logic

## Key Functions
### getHUI
- Purpose: Retrieves HordeUpdateInterface from an object's behavior modules
- Calls: None (accessor)

### PartitionFilterHordeMember::allow
- Purpose: Determines if an object should be considered part of the horde
- Calls: getHUI, getTemplate, isKindOfMulti, getRelationship, isOffMap

### HordeUpdate::update
- Purpose: Main update loop that checks horde status and applies effects
- Calls: getHordeUpdateModuleData, showHideFlag, evaluateMoraleBonus, setTerrainDecal, setTerrainDecalSize, setTerrainDecalFadeTarget

### HordeUpdate::joinOrLeaveHorde
- Purpose: Handles state transitions when entering/leaving a horde
- Calls: evaluateMoraleBonus

## Globals
- **DEFAULT_UPDATE_RATE (Int)**: Default update rate for horde checks (LOGICFRAMES_PER_SECOND)

## Dependencies
- PartitionManager.h (for spatial queries)
- AIUpdate.h (for morale evaluation)
- Drawable.h (for visual effects)
- Common game types (Player, ThingTemplate, Upgrade)
- INI parsing utilities
- Xfer.h (for serialization)
