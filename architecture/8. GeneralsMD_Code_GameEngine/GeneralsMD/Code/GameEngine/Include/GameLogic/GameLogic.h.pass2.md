# GeneralsMD/Code/GameEngine/Include/GameLogic/GameLogic.h - Enhanced Analysis

## Architectural Role
Core game state manager that orchestrates object lifecycle, game updates, and state transitions. Acts as the central hub for game logic coordination, bridging between rendering, AI, and networking subsystems.

## Cross-References
### Incoming
- GameEngine subsystems (AI, rendering, networking) call into GameLogic for object management and game state queries
- UI systems reference GameLogic for game mode checks and progress tracking
- Audio systems likely use GameLogic for game state-dependent sound triggers

### Outgoing
- Calls into UpdateModule system for game updates
- Interfaces with TerrainLogic and GhostObjectManager for spatial queries
- Uses LoadScreen for game initialization
- Manages CommandList processing for player actions

## Design Patterns
- **Singleton**: GameLogic is the sole instance managing global game state
- **Priority Queue**: Uses vector as a priority queue for sleepy updates (commented implementation details)
- **Observer**: Implicit event system via object registration and command processing (not explicitly shown but inferred from structure)
