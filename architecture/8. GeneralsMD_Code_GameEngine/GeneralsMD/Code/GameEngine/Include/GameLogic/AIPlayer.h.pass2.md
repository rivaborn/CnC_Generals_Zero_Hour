# GeneralsMD/Code/GameEngine/Include/GameLogic/AIPlayer.h - Enhanced Analysis

## Architectural Role
Central AI controller that orchestrates base building, unit production, and strategic decision-making. Bridges between high-level AI logic and game object interactions, managing production queues and resource allocation.

## Cross-References
### Incoming
- **Player.h**: Likely instantiates AIPlayer for computer-controlled players
- **GameLogic/Team.h**: Uses Team/TeamPrototype for unit group management
- **GameLogic/ThingTemplate.h**: References unit/building templates for production
- **GameLogic/BuildListInfo.h**: External build planning data structure

### Outgoing
- **GameLogic/Object.h**: Interacts with game objects (units/structures)
- **GameLogic/Team.h**: Manages team formation and deployment
- **GameLogic/Waypoint.h**: Uses waypoints for pathfinding/repair logic
- **Common/GameMemory.h**: Memory pool allocation
- **Common/Snapshot.h**: Save/load serialization

## Design Patterns
- **Command Pattern**: WorkOrder encapsulates production commands for deferred execution
- **State Pattern**: AI behavior varies by difficulty (m_difficulty) and game phase
- **Observer Pattern**: Event handlers (onUnitProduced/onStructureProduced) react to game state changes

*Not inferable*: Exact strategy pattern implementation for team selection.
