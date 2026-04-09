# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/camera.h - Enhanced Analysis

## Architectural Role
This file defines the core camera system for the SAGE engine, bridging rendering and scene management. It provides the mathematical foundation for view transformations, frustum culling, and coordinate space conversions that are critical for both the rendering pipeline and spatial partitioning systems.

## Cross-References
### Incoming
- Rendering subsystem calls `Project()` for screen-space calculations
- Scene graph uses `Cull_Sphere()` for occlusion culling
- Animation system invokes `Set_Transform()` for camera attachments

### Outgoing
- Relies on `CollisionMath` for spatial queries
- Uses `FrustumClass` and `PlaneClass` for visibility testing
- Depends on `Matrix4` for projection calculations

## Design Patterns
- **Lazy Evaluation**: Frustum updates are deferred via `Update_Frustum()` cache invalidation
- **Composite**: Camera inherits from `RenderObjClass` despite not rendering, enabling scene graph integration
- **Strategy**: Projection type (perspective/orthographic) is encapsulated as an enum with runtime selection

*Not inferable*: Exact observer pattern implementation for transform changes.
