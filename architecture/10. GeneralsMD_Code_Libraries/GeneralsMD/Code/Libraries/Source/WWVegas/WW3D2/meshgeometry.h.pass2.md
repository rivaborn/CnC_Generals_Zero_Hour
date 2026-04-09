# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.h - Enhanced Analysis

## Architectural Role
This file defines the core `MeshGeometryClass`, which serves as the foundational data structure for 3D mesh geometry in the SAGE engine. It bridges the rendering pipeline (WW3D) with collision detection and animation systems, providing the geometric backbone for all in-game models.

## Cross-References
### Incoming
- **Rendering System**: Uses `RenderInfoClass` for screen-space vertex deformation.
- **Collision System**: Called by `RayCollisionTestClass`, `AABoxCollisionTestClass`, and `OBBoxCollisionTestClass` for intersection tests.
- **Animation System**: Interfaces with `HTreeClass` for skinning/deformation.
- **W3D File I/O**: `ChunkLoadClass` for loading mesh data from W3D files.

### Outgoing
- **Bounding Volumes**: Depends on `AABoxClass`, `OBBoxClass`, and `SphereClass` for spatial queries.
- **Culling**: Uses `AABTreeClass` for hierarchical culling.
- **Memory Management**: Relies on `ShareBufferClass` for dynamic array allocation.

## Design Patterns
- **Composite**: `MeshGeometryClass` aggregates geometric primitives (vertices, polygons) and behavior (collision, deformation).
- **Flyweight**: `ShareBufferClass` usage suggests shared memory management for vertex/polygon data.
- **Strategy**: Optimized collision paths (`cast_aabox_identity`, `cast_aabox_z90`) demonstrate runtime algorithm selection based on transform state.

*Not inferable*: Exact inheritance hierarchy of `W3DMPO`/`RefCountClass`/`MultiListObjectClass`.
