# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/RailedTransportAIUpdate.cpp

## Purpose
Handles AI logic for railed transport units, managing waypoint paths and transit states.

## Responsibilities
- Loads and manages waypoint paths for railed transports
- Controls transit between waypoints
- Manages dock state during transit
- Handles AI commands for transport operations

## Key Types
- `RailedTransportAIUpdateModuleData` (Class): Stores module configuration (path prefix name)
- `RailedTransportAIUpdate` (Class): Main AI update module for railed transports
- `INVALID_PATH` (const Int): Sentinel value for invalid path (-1)

## Key Functions
### `loadWaypointData`
- Purpose: Loads waypoint paths from terrain logic
- Calls: `TheTerrainLogic->getWaypointByName`

### `pickAndMoveToInitialLocation`
- Purpose: Selects closest path and moves to its end waypoint
- Calls: `aiFollowWaypointPath`, `TheTerrainLogic->getWaypointByID`

### `update`
- Purpose: Main update loop for railed transport AI
- Calls: `AIUpdateInterface::update`, `loadWaypointData`, `pickAndMoveToInitialLocation`, `getCurLocomotor->setUltraAccurate`

### `privateExecuteRailedTransport`
- Purpose: Initiates transport along next waypoint path
- Calls: `aiFollowWaypointPath`, `TheTerrainLogic->getWaypointByID`

### `privateEvacuate`
- Purpose: Handles evacuation/unloading commands
- Calls: `rtdui->unloadAll`

## Globals
- `INVALID_PATH` (const Int): Sentinel value for invalid path

## Dependencies
- `PreRTS.h`, `ThingTemplate.h`, `GameState.h`, `Locomotor.h`, `RailedTransportAIUpdate.h`, `RailedTransportDockUpdate.h`, `Object.h`
- `AIUpdateInterface`, `AIUpdateModuleData`, `Waypoint`, `TheTerrainLogic`, `Xfer`, `SC_INVALID_DATA`
