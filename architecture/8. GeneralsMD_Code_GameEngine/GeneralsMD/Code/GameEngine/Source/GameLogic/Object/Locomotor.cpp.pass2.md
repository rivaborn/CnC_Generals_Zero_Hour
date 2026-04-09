# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Locomotor.cpp - Enhanced Analysis

## Architectural Role
This file implements the core locomotion system for game objects, bridging physics simulation, pathfinding, and AI movement behaviors. It serves as the runtime controller for movement templates defined in the data files, handling surface-specific movement logic and force calculations.

## Cross-References
### Incoming
- **AIPathfind.cpp**: Uses locomotion data for path validation
- **PhysicsUpdate.cpp**: Applies movement forces calculated here
- **AIUpdate.cpp**: Requests movement behaviors for units
- **Object.cpp**: Uses LocomotorSet for object movement

### Outgoing
- **W3D Math Library**: Vector/Matrix operations for 3D movement
- **PartitionManager**: Spatial queries for movement validation
- **BodyModule**: Physical body state updates
- **INI System**: Loads locomotion templates from data files

## Design Patterns
- **Template Method**: LocomotorTemplate defines movement algorithms while Locomotor implements them
- **Strategy**: Different locomotion types (thrust/wings/wheels) are interchangeable strategies
- **Flyweight**: TheLocomotorStore caches and reuses locomotion templates

*Not inferable*: Exact observer relationships with physics/AI systems.
