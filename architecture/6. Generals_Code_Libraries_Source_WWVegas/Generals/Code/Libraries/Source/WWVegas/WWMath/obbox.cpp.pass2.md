# Generals/Code/Libraries/Source/WWVegas/WWMath/obbox.cpp - Enhanced Analysis

## Architectural Role
Core collision detection component in the WWMath library, providing oriented bounding box (OBBox) geometry and intersection tests. Used throughout the physics and game logic systems for spatial queries and collision resolution.

## Cross-References
### Incoming
- `colmathobbox.cpp` (uses OBBox collision functions)
- Physics system (likely calls intersection tests)
- Game object movement/positioning logic

### Outgoing
- `vector3.h` (math operations)
- `matrix3.h` (transformations)
- `tri.h` (triangle collision)
- `aabox.h` (axis-aligned box conversions)

## Design Patterns
- **Separating Axis Theorem (SAT)**: Used for OBBox-OBBox and OBBox-triangle collision detection, providing efficient intersection tests.
- **Component-based geometry**: OBBox encapsulates center, basis, and extent as separate data members for modularity.
- **Axis-aligned projection**: Core technique for all intersection tests, projecting geometry onto test axes.

*Not inferable: Factory pattern or object pooling not evident in this file.*
