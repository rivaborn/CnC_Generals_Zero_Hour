# Generals/Code/Libraries/Source/WWVegas/WWMath/obbox.h - Enhanced Analysis

## Architectural Role
This file defines the core `OBBoxClass` used for 3D collision detection in the SAGE engine. It bridges the math library with game systems requiring spatial queries, particularly for unit/building collision and pathfinding.

## Cross-References
### Incoming
- Physics system (collision resolution)
- Pathfinding (obstacle representation)
- Unit/building placement validation

### Outgoing
- `vector3.h`, `matrix3.h`, `matrix3d.h` (math primitives)
- `TriClass`, `AABoxClass`, `PlaneClass` (collision geometry)

## Design Patterns
- **Data-Oriented Design**: Stores box data (center, extents, basis) in contiguous memory for cache efficiency.
- **Separation of Concerns**: Pure math operations without game logic, allowing reuse across subsystems.
- **Inline Functions**: Critical methods inlined for performance in collision-heavy scenarios.

*Not inferable*: No clear use of object pooling or event-driven patterns.
