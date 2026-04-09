# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BridgeBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the bridge behavior system, acting as an intermediary between the terrain system (which manages bridge geometry) and the object system (which handles game entities). It bridges (pun intended) the gap between static terrain features and dynamic game objects, ensuring bridges function as both navigable terrain and destructible objects.

## Cross-References
### Incoming
- **TerrainLogic**: Uses bridge behavior to update bridge state when terrain changes
- **AIPathfind**: Queries bridge state for pathfinding decisions
- **ObjectCreationList**: Uses bridge behavior to spawn/destroy bridge-related objects
- **FXList**: References bridge destruction effects defined here

### Outgoing
- **TerrainLogic**: Queries bridge position and updates bridge info
- **AIPathfind**: Notifies pathfinder of bridge state changes
- **ThingFactory**: Creates scaffold objects during bridge construction
- **BridgeScaffoldBehavior**: Manages scaffold object behavior
- **Xfer**: Handles serialization of bridge state

## Design Patterns
- **Strategy Pattern**: Bridge behavior modules can be swapped based on bridge state (intact/damaged/destroyed)
- **Observer Pattern**: Bridge behavior notifies pathfinder of state changes
- **Composite Pattern**: Manages collection of scaffold objects as part of bridge behavior

*Not inferable*: Exact implementation of Command pattern for bridge destruction sequence.
