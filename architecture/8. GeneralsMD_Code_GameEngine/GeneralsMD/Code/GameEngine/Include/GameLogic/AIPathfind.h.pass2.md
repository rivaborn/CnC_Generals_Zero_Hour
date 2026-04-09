# GeneralsMD/Code/GameEngine/Include/GameLogic/AIPathfind.h - Enhanced Analysis

## Architectural Role
This header defines the core pathfinding system that bridges AI decision-making and movement execution. It provides spatial reasoning for units, handling obstacle avoidance, terrain classification, and hierarchical pathfinding across different layers (ground, bridges, walls).

## Cross-References
### Incoming
- AI behavior modules (e.g., `AIBehavior.h`) use `Pathfinder::findPath` for movement planning
- Unit movement systems call `validMovementPosition` for collision checks
- Game logic updates use `classifyMapCell` during world state changes

### Outgoing
- Relies on `LocomotorSet` for unit movement capabilities
- Interacts with `GameLogic` for object state queries
- Uses `PathfindZoneManager` for zone-based pathfinding optimizations

## Design Patterns
- **Strategy Pattern**: Different pathfinding strategies (A*, hierarchical) can be selected
- **Observer Pattern**: Pathfinding map updates when objects enter/leave cells
- **Flyweight Pattern**: `PathfindCell` instances reused across the grid

*Not inferable*: Exact implementation of A* algorithm details.
