# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tri.cpp - Enhanced Analysis

## Architectural Role
This file provides core geometric utilities for triangle operations, critical for collision detection and spatial queries in the SAGE engine. It bridges the WWMath library with higher-level systems like collision math and rendering.

## Cross-References
### Incoming
- **Collision Detection**: `colmathaabtri.cpp` and `colmathobbtri.cpp` use `find_dominant_plane` and `TriClass::Contains_Point` for triangle-AABB/OBB intersection tests.
- **Rendering**: Likely used by W3D model processing for triangle culling or LOD calculations (not explicitly referenced in provided context).

### Outgoing
- **WWMath**: Uses `WWMath::Fabs` for magnitude comparisons.
- **Vector2/Vector3**: Depends on these for 2D/3D vector operations in point-in-triangle tests.

## Design Patterns
- **Strategy Pattern**: Multiple implementations of point-in-triangle tests (cross-product, barycentric) are encapsulated within `Contains_Point`, selectable via preprocessor flags.
- **Utility Class**: `TriClass` acts as a container for triangle-related operations, promoting code reuse across subsystems.
- **Optimization via Dominant Plane**: Uses dominant plane detection to reduce 3D problems to 2D, improving performance in collision checks.

*Not inferable*: Exact usage in rendering pipeline or AI pathfinding.
