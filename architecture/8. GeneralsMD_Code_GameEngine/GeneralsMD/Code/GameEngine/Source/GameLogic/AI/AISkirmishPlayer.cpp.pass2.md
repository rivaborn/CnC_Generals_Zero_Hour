# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AISkirmishPlayer.cpp - Enhanced Analysis

## Architectural Role
This file implements the skirmish AI player, extending the base AIPlayer class with skirmish-specific logic like base defense management, superweapon targeting, and build list adjustments. It integrates with the AI framework, game logic, and terrain systems to create autonomous opponents.

## Cross-References
### Incoming
- **AI.cpp**: Likely instantiates AISkirmishPlayer for skirmish mode
- **GameLogic.cpp**: May call processBaseBuilding/processTeamBuilding during game updates
- **Networking**: Xfer/crc methods called during save/load or network sync

### Outgoing
- **AIPathfind.h**: Uses pathfinding for superweapon targeting
- **TerrainLogic.h**: Queries waypoints and structure bounds
- **BuildAssistant.h**: Checks unit production feasibility
- **ScriptEngine.h**: May use for dynamic AI behavior

## Design Patterns
- **Template Method**: Extends AIPlayer with skirmish-specific implementations
- **Strategy**: Build list rotation based on starting position (adjustBuildList)
- **State**: Tracks defense angles and enemy state for tactical decisions

*Not inferable*: Exact event-driven or ECS integration not visible in this file.
