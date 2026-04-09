# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathaabtri.cpp - Enhanced Analysis

## Architectural Role
This file implements core collision detection logic for AABB-triangle interactions, serving as a foundational component for the game's physics system. It's optimized for the SAGE engine's rendering and game logic needs, particularly for terrain and object collisions.

## Cross-References
### Incoming
- Physics system (likely calls `CollisionMath::Intersection_Test` for dynamic collision checks)
- Terrain rendering (uses AABB-triangle tests for ground collision)
- Projectile/unit movement systems (depends on collision normals)

### Outgoing
- Uses `Vector3` operations (dot/cross products) from WWMath
- Relies on `AABoxClass` and `TriClass` definitions
- Calls into `WWMath` for floating-point operations and constants

## Design Patterns
- **Static Context Pattern**: Uses static scratchpad structs (`BTCollisionStruct`, `AABTIntersectStruct`) to avoid allocation overhead, though noted as thread-unsafe
- **Separating Axis Theorem**: Implements multiple axis tests to determine collision, optimized for AABB's axis-aligned nature
- **Optimized Projection**: Precomputes edge vectors and cross products to minimize runtime calculations during collision checks
