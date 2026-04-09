# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdmesh.h - Enhanced Analysis

## Architectural Role
This file defines the core shaded mesh class (`ShdMeshClass`) in the SAGE engine's rendering pipeline, bridging legacy W3D mesh loading with the new shader system. It serves as a render object container for sub-meshes, handling lighting, collision, and culling optimizations.

## Cross-References
### Incoming
- Rendering system (calls `Render`, `Special_Render`)
- Collision detection (calls `Cast_Ray`, `Cast_AABox`, etc.)
- W3D loading pipeline (calls `Load_W3D`)
- Lighting system (calls `Set_Lighting_Environment`)

### Outgoing
- Sub-mesh management (`ShdSubMeshClass`)
- Lighting environment (`LightEnvironmentClass`)
- Texture projection (`TexProjectClass`)
- Legacy mesh conversion (`MeshClass`)

## Design Patterns
- **Composite Pattern**: `ShdMeshClass` contains multiple `ShdSubMeshStruct` instances, treating them uniformly.
- **Bridge Pattern**: Separates abstraction (`ShdMeshClass`) from implementation (`ShdSubMeshClass`/`ShdRendererNodeClass`).
- **Dependency Injection**: Lighting environment and texture projector are injected via setters.
