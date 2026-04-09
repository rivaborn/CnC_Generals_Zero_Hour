# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathaabtri.cpp - Enhanced Analysis

## Architectural Role
This file implements the core collision detection logic between axis-aligned bounding boxes (AABB) and triangles, a fundamental operation in the physics system. It's part of the broader collision detection subsystem that handles various primitive-primitive interactions.

## Cross-References
### Incoming
- Physics system components (e.g., rigid body simulation)
- Spatial partitioning code (for broad-phase collision detection)
- Game object movement/positioning logic

### Outgoing
- Vector3 operations (dot products, cross products, vector math)
- WWMath utility functions (epsilon comparisons, absolute value)
- Other collision detection modules (for more complex interactions)

## Design Patterns
- **Separating Axis Theorem (SAT)**: Used to determine collision by testing separation along multiple axes
- **Static Context Object**: Uses static instances of BTCollisionStruct and AABTIntersectStruct to avoid repeated allocations
- **Axis-Aligned Optimization**: Exploits AABB's axis alignment to simplify many calculations compared to general OBB-OBB collision

The SAT implementation is particularly notable as it's optimized for AABB-triangle interactions, reducing the number of required dot products compared to the general OBB-OBB case. The static context objects suggest performance optimization was a priority, though this makes the code non-thread-safe as noted in the comments.
