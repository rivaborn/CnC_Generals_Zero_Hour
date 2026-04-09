# Generals/Code/Libraries/Source/WWVegas/WW3D2/intersec.inl - Enhanced Analysis

## Architectural Role
This file provides core 3D intersection and clipping utilities for the SAGE engine's rendering pipeline, bridging screen-space input (mouse clicks) with world-space geometry. It's critical for hit-testing, decal projection, and spatial queries used by both gameplay and UI systems.

## Cross-References
### Incoming
- Rendering system (for ray casting from screen coordinates)
- Gameplay systems (for unit/building selection via hit-testing)
- Decal/particle systems (for intersection with world geometry)

### Outgoing
- Camera system (`camera.h` for view transformation)
- Math utilities (`Vector3`/`Vector2` for geometric operations)
- Debug subsystem (conditional debug printing)

## Design Patterns
- **Inline Template Method**: Core intersection logic is inlined for performance-critical path optimization
- **Spatial Decomposition**: Specialized functions for Z-axis aligned operations (e.g., `_Point_In_Polygon_Z`)
- **Parameter Object**: `IntersectionClass` encapsulates intersection state (ray, results) for reuse

*Not inferable*: Exact usage patterns of `IntersectionResultClass` or how results are consumed by callers.
