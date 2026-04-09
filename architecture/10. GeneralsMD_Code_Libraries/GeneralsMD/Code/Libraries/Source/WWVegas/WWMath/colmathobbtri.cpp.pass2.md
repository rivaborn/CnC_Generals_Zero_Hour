# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathobbtri.cpp - Enhanced Analysis

## Architectural Role
This file implements core collision detection logic between oriented bounding boxes (OBBox) and triangles, serving as a foundational component for the game's physics system. It handles both separation tests and intersection checks, providing critical data for game object interactions.

## Cross-References
### Incoming
- Physics system (likely calls `CollisionMath::Intersection_Test` and collision response functions)
- Game object movement/positioning logic (uses collision data for pathfinding/obstacle avoidance)
- Projectile/targeting systems (relies on OBBox-triangle intersection tests)

### Outgoing
- Uses `Vector3` class operations (dot products, cross products, length calculations)
- Depends on `OBBoxClass` and `TriClass` definitions from included headers
- Leverages `WWMath` namespace utilities (e.g., `Fabs`)

## Design Patterns
- **Context Object Pattern**: Uses `BTCollisionStruct` and `BTIntersectStruct` to encapsulate collision test state
- **Separating Axis Theorem**: Implements the mathematical approach for convex collision detection
- **Strategy Pattern**: Different axis tests are implemented as separate functions that can be selected at runtime

*Not inferable*: Exact usage patterns in game logic (e.g., frequency of calls, typical object types involved)
