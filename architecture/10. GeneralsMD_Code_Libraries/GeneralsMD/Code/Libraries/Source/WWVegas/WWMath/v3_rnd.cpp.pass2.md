# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/v3_rnd.cpp - Enhanced Analysis

## Architectural Role
This file provides the core random vector generation utilities for the SAGE engine's 3D math system, enabling procedural placement of game entities, particle effects, and AI behavior patterns. The rejection sampling approach ensures physically plausible distributions within geometric primitives.

## Cross-References
### Incoming
- **Physics System**: Uses random vectors for force application and collision response
- **Particle System**: Generates initial velocities and positions for effects
- **AI Pathfinding**: Creates random waypoints and patrol routes
- **Game Object Placement**: Randomizes spawn positions for units/structures

### Outgoing
- **WWMath Library**: Uses `Vector3`, `Vector2`, and `WWMath::Inv_Sqrt()`
- **Random Number Generation**: Depends on `Random3Class` for core RNG

## Design Patterns
- **Rejection Sampling**: Used in sphere/cylinder generation to ensure points lie within bounds
- **Strategy Pattern**: Different randomizer classes implement `Get_Vector` for various shapes
- **Singleton**: Global `Randomizer` instance for thread-safe RNG access (not inferable if unsafe)
