# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/NeutronBlastBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the neutron blast effect behavior, a game-specific weapon effect that triggers when a projectile dies. It integrates with the partition system for spatial queries and the containment system for nested object handling, demonstrating how game logic components interact with spatial and hierarchical game object management.

## Cross-References
### Incoming
- **DamageModule**: Calls `onDie` when objects are destroyed
- **PartitionManager**: Used for spatial queries to find affected objects
- **ContainModule**: Called to handle nested objects within containers
- **AIUpdate**: Used for pilot behavior when vehicles are affected

### Outgoing
- **GameLogic**: For deselecting affected objects
- **PlayerList**: For accessing neutral player team
- **Drawable**: For clearing terrain decals
- **Object**: For various object state modifications

## Design Patterns
- **Strategy Pattern**: The neutron blast behavior is implemented as a module that can be attached to different objects, allowing different blast configurations
- **Visitor Pattern**: The `neutronBlastToObject` method acts as a visitor that applies different effects based on object type (infantry, vehicles, containers)
- **Observer Pattern**: The `onDie` method acts as an observer for object death events
