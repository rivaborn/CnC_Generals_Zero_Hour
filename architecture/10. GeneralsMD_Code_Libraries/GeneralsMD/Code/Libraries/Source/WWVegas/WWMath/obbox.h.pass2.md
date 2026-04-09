# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/obbox.h - Enhanced Analysis

## Architectural Role
This file defines the core `OBBoxClass` for oriented bounding box operations, critical for collision detection in the SAGE engine. It bridges the math library with game logic by providing spatial queries used in physics, pathfinding, and unit interactions.

## Cross-References
### Incoming
- **Physics/Simulation**: Likely called by `GeneralsMD/Code/Game/Logic/Physics` for collision resolution.
- **AI/Pathfinding**: Used in `GeneralsMD/Code/Game/Logic/AI` for obstacle avoidance.
- **Rendering**: Possibly referenced in `GeneralsMD/Code/Libraries/Source/WWVegas/W3D` for frustum culling.

### Outgoing
- **Math Library**: Depends on `vector3.h`, `matrix3.h`, and `matrix3d.h` for vector/matrix operations.
- **Collision Subsystem**: Interfaces with `TriClass` and `AABoxClass` for broader collision checks.

## Design Patterns
- **Data-Oriented Design**: Stores box data (center, extents, basis) in contiguous memory for cache efficiency.
- **Inline Functions**: Critical methods like `Project_To_Axis` are inlined to avoid overhead in collision checks.
- **Separation of Concerns**: Collision logic (`Oriented_Boxes_Intersect`) is isolated from transformation logic (`Transform`).

*Not inferable*: No clear use of visitor, factory, or observer patterns.
