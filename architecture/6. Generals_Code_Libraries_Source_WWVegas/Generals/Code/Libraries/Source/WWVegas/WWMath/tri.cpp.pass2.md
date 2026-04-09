# Generals/Code/Libraries/Source/WWVegas/WWMath/tri.cpp - Enhanced Analysis

## Architectural Role
This file provides core geometric utilities for triangle operations, critical for collision detection and spatial queries in the physics and rendering subsystems. Its functions are foundational for determining triangle orientation and point containment, which are used extensively in the game's collision math pipeline.

## Cross-References
### Incoming
- **Collision Detection**: `colmathaabtri.cpp` and `colmathobbtri.cpp` use `TriClass::Find_Dominant_Plane` and `TriClass::Contains_Point` for triangle-based collision tests.
- **Physics System**: Likely called by physics-related modules for spatial queries involving triangles.

### Outgoing
- **WWMath Utilities**: Relies on `WWMath::Fabs` for absolute value operations.
- **Vector2 Operations**: Uses `Vector2` class for 2D cross-product calculations in point-in-triangle tests.

## Design Patterns
- **Utility Class**: `TriClass` encapsulates triangle-specific operations, promoting code reuse and separation of concerns.
- **Lookup Table Optimization**: Uses a static `dominance` table in `find_dominant_plane_fast` to avoid runtime branching, improving performance for dominant plane detection.
- **Inline Functions**: `find_dominant_plane_fast` is marked `static inline` to reduce function call overhead in hot paths like collision detection.

**Not inferable**: No clear use of other patterns (e.g., no factories, observers, or decorators visible in this file).
