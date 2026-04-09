# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/RailedTransportAIUpdate.cpp

## Purpose
This file contains the implementation for the AI update logic of railed transport objects in Command & Conquer Generals. It handles pathfinding, movement, and docking operations for these vehicles.

## Responsibilities
- Manage waypoint paths for railed transports.
- Handle initial positioning and movement to waypoints.
- Control docking operations based on transport status.
- Process AI commands related to transport execution and evacuation.

## Key Types
- `RailedTransportAIUpdateModuleData`: Stores configuration data for railed transport AI updates.
- `RailedTransportAIUpdate`: Manages the AI logic for railed transports, including pathfinding and docking.

## Key Functions
### RailedTransportAIUpdate::loadWaypointData
- Purpose: Loads waypoint paths from the game's terrain logic.
- Calls: `TheTerrainLogic->getWaypointByName`

### RailedTransportAIUpdate::pickAndMoveToInitialLocation
- Purpose: Selects and moves the transport to the closest initial waypoint path.
- Calls: `aiFollowWaypointPath`, `DEBUG_ASSERTCRASH`

### RailedTransportAIUpdate::update
- Purpose: Updates the transport's state, including movement and docking status.
- Calls: `loadWaypointData`, `AIUpdateInterface::update`, `setInTransit`

### RailedTransportAIUpdate::aiDoCommand
- Purpose: Processes AI commands for the transport.
- Calls: `isAllowedToRespondToAiCommands`, `AIUpdateInterface::aiDoCommand`

## Globals
- `INVALID_PATH (Int)`: Represents an invalid path index.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/ThingTemplate.h"
  - "Common/GameState.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Module/RailedTransportAIUpdate.h"
  - "GameLogic/Module/RailedTransportDockUpdate.h"
  - "GameLogic/Object.h"

- External symbols used:
  - `TheTerrainLogic`
  - `CMD_FROM_AI`
  - `AICMD_EXECUTE_RAILED_TRANSPORT`
  - `AICMD_EVACUATE`
  - `UPDATE_SLEEP_NONE`
  - `SC_INVALID_DATA`
