# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/ChinookAIUpdate.cpp

## Purpose
Implements AI behavior for the Chinook helicopter unit, handling states like takeoff, landing, combat drops, and evacuation.

## Responsibilities
- Manages Chinook-specific AI states (takeoff, landing, combat drop, evacuation)
- Controls passenger interactions (attack commands, evacuation)
- Handles flight status and position adjustments
- Manages rope mechanics for combat drops
- Implements supply boost upgrades

## Key Types
- **ChinookAIStateType (Enum)**: Defines Chinook-specific AI states (TAKING_OFF, LANDING, etc.)
- **ChinookEvacuateState (Class)**: Handles passenger evacuation logic
- **ChinookHeadOffMapState (Class)**: Manages Chinook exiting the map
- **ChinookTakeoffOrLandingState (Class)**: Controls takeoff/landing animations and physics
- **ChinookCombatDropState (Class)**: Manages combat drop rope mechanics and rappelling
- **RopeInfo (Struct)**: Stores rope state data for combat drops

## Key Functions
### `calcDistSqr`
- Purpose: Calculates squared distance between two 3D coordinates
- Calls: None

### `getPotentialRappeller`
- Purpose: Finds a rappellable passenger in the Chinook
- Calls: `getContain()`, `getContainedItemsList()`

### `getPP`
- Purpose: Not inferable (truncated in source)
- Calls: Not inferable

## Globals
- **BIGNUM (Real)**: Large constant value (99999.0f) for physics limits

## Dependencies
- Common modules: ActionManager, GameState, Team, ThingFactory
- GameClient: Drawable, GameClient, ParticleSys
- GameLogic: AIPathfind, Locomotor, ContainModule, PhysicsUpdate
- Key includes: "PreRTS.h", "Common/ActionManager.h", "GameLogic/Module/ChinookAIUpdate.h"
