# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.cpp - Enhanced Analysis

## Architectural Role
This file implements the decal rendering subsystem for the SAGE engine, handling both static (rigid) and animated (skinned) decals. It bridges the gap between the decal system (`decalsys.h`) and the rendering pipeline (`dx8wrapper.h`), managing geometry clipping, material processing, and vertex deformation for skinned meshes.

## Cross-References
### Incoming
- `decalsys.h` - Uses `DecalMeshClass` as base for decal management
- `mesh.h`/`meshmdl.h` - References mesh structures for vertex/normal data
- `DX8Wrapper` - Called by `Render()` methods for actual drawing

### Outgoing
- `PlaneClass` - For polygon clipping operations
- `MaterialPassClass` - For shader/texture management
- `Vector3`/`Matrix3D` - Core math utilities

## Design Patterns
- **Composite Pattern**: `DecalMeshClass` hierarchy (Rigid/Skin variants) with shared rendering logic
- **Flyweight Pattern**: Reuses vertex data across multiple decals via `ParentVertexIndices`
- **Object Pooling**: Temporary `DecalPolyClass` instances for clipping operations

*Not inferable*: Exact memory management strategy for decal resources.
