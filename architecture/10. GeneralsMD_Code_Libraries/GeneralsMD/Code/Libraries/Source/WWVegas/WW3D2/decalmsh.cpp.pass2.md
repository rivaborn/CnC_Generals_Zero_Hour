# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.cpp - Enhanced Analysis

## Architectural Role
This file implements the decal rendering subsystem for the SAGE engine's 3D rendering pipeline. It bridges between the decal system and the DirectX8 rendering backend, handling both static (rigid) and animated (skinned) mesh decals. The decal system is critical for environmental effects like bullet impacts and explosions.

## Cross-References
### Incoming
- `decalsys.cpp` (DecalSystemClass) - Creates and manages decal instances
- `meshmdl.cpp` (MeshModelClass) - Attaches decal meshes to 3D models
- `rinfo.cpp` (RenderInfoClass) - Provides rendering context for decal processing

### Outgoing
- `dx8wrapper.cpp` - DirectX8 state management (textures, materials, shaders)
- `mesh.cpp` - Vertex deformation for skinned meshes
- `texture.cpp` - Texture reference management
- `material.cpp` - Material reference counting

## Design Patterns
- **Composite Pattern**: DecalMeshClass hierarchy (RigidDecalMeshClass/SkinDecalMeshClass) encapsulates different decal types while providing uniform interface
- **Flyweight Pattern**: Reuses vertex data across multiple decals to reduce memory usage
- **Observer Pattern**: DecalGeneratorClass notifies decal meshes of changes via Add_Mesh callback

Rules followed. Output under 400 tokens.
