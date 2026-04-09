# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIPathfind.cpp - Enhanced Analysis

## Architectural Role
This file implements the core pathfinding system for AI units, bridging the gap between high-level AI behavior (AI.cpp) and low-level movement mechanics (Locomotor.h). It handles both strategic path planning and real-time obstacle avoidance, with specializations for attack paths and repulsor-based navigation.

## Cross-References
### Incoming
- **AI.cpp**: Uses pathfinding results for unit movement decisions
- **BehaviorTree.cpp**: Consumes path data for tactical behaviors
- **Unit.cpp**: Requests paths for individual unit navigation
- **GameLogic.cpp**: Manages pathfinding zones and global state

### Outgoing
- **Locomotor.h**: Validates surface movement capabilities
- **PartitionManager.h**: Spatial queries for obstacle detection
- **TerrainLogic.h**: Elevation and surface type checks
- **W3D Rendering**: Debug visualization hooks (debugShowSearch)

## Design Patterns
- **State Pattern**: Pathfinding cells maintain state (open/closed) during search
- **Visitor Pattern**: Movement validation via TCheckMovementInfo struct
- **Flyweight Pattern**: PathNode reuse for optimization (m_nextOpti caching)

*Not inferable*: Exact optimization strategy for m_nextOptiDirNorm2D normalization.
