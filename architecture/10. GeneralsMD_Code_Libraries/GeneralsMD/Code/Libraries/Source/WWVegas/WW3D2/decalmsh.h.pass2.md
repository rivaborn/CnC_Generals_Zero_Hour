# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.h - Enhanced Analysis

## Architectural Role
This header defines the decal system's core classes, bridging the rendering pipeline (W3D) with dynamic mesh modifications. It enables damage effects, bullet holes, and other temporary surface alterations while maintaining separation between static geometry and decals.

## Cross-References
### Incoming
- **Rendering System**: Likely called by `RenderInfoClass` or similar during scene traversal
- **Decal Management**: Used by `DecalSystemClass` to organize decals across multiple meshes
- **Game Logic**: Called by projectile/weapon systems when applying decals (e.g., bullet impacts)

### Outgoing
- **Mesh System**: Depends on `MeshClass` for parent geometry access
- **Material System**: Uses `ShaderClass` and `VertexMaterialClass` for visual properties
- **Geometry Utilities**: Relies on `OBBoxClass` for spatial queries

## Design Patterns
- **Strategy Pattern**: Abstract `DecalMeshClass` with concrete implementations (`RigidDecalMeshClass`, `SkinDecalMeshClass`) for different mesh types
- **Composite Pattern**: `NextVisible` pointer suggests decal meshes form a linked list for efficient rendering
- **Resource Management**: `RefCountClass` inheritance indicates shared ownership semantics for decal meshes
