# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/frustum.cpp - Enhanced Analysis

## Architectural Role
This file implements the core frustum initialization logic for the SAGE engine's rendering pipeline, bridging camera transforms and view frustum geometry. It's critical for visibility culling and spatial partitioning in the game's rendering and collision systems.

## Cross-References
### Incoming
- `colmathfrustum.cpp` - Uses `FrustumClass` for overlap tests with various geometric primitives (AABox, OBBox, points, spheres, triangles)
- Likely called by rendering subsystems (e.g., `W3D` or scene management) during view frustum setup

### Outgoing
- Depends on `Matrix3D`, `Vector2/3`, `PlaneClass` from `WWMath` library
- Uses `Vector3::Cross_Product`, `Vector3::Dot_Product`, `Matrix3D::Transform_Vector`, `PlaneClass::Set`

## Design Patterns
- **Factory Method**: `FrustumClass::Init` acts as a constructor-like method to initialize frustum state
- **Data Transfer Object**: `FrustumClass` encapsulates frustum geometry (corners, planes, bounds) for reuse in collision tests
- **Coordinate System Handling**: Explicitly manages right-handed vs. reflected camera matrices (cross-product validation)
