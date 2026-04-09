# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RailedTransportAIUpdate.h

## Purpose
Defines AI module for managing railed transport units (e.g., trains) in the game.

## Responsibilities
- Manages waypoint-based movement for railed transports
- Handles transport commands and evacuation logic
- Loads and tracks waypoint paths for navigation
- Controls transit state and initial positioning

## Key Types
- **Waypoint (Class)**: Not inferable (forward reference).
- **RailedTransportAIUpdateModuleData (Class)**: Module data containing path prefix name.
- **RailedTransportAIUpdate (Class)**: Main AI update class for railed transports.
- **RailedTransportAIUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **RailedTransportAIUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).
- **WaypointPathInfo (Class)**: Stores start/end waypoint IDs for a path.
- **(anonymous enum) (Enum)**: Not inferable (likely internal macro enum).
- **MAX_WAYPOINT_PATHS (Enum)**: Constant defining max path count (32).

## Key Functions
### RailedTransportAIUpdate::aiDoCommand
- Purpose: Handles AI commands for the transport.
- Calls: `privateExecuteRailedTransport`, `privateEvacuate`.

### RailedTransportAIUpdate::update
- Purpose: Updates transport state (sleep time logic).
- Calls: Not inferable.

### RailedTransportAIUpdate::privateExecuteRailedTransport
- Purpose: Executes railed transport logic.
- Calls: Not inferable.

### RailedTransportAIUpdate::privateEvacuate
- Purpose: Handles evacuation of transport.
- Calls: Not inferable.

### RailedTransportAIUpdate::loadWaypointData
- Purpose: Loads waypoint paths from the map
