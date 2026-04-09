# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdsubmesh.cpp

## Purpose
Handles sub-mesh data loading, initialization, and rendering for the WWShade shader system, supporting both legacy W3D meshes and modern shader-based rendering.

## Responsibilities
- Loads W3D mesh data (vertices, normals, UVs, tangents, etc.)
- Manages shader assignments and material properties
- Supports skinning and deformation for animated meshes
- Handles legacy mesh conversion to shader-based rendering
- Maintains vertex buffers and polygon data

## Key Types
- **ShdSubMeshClass (Class)**: Main class handling sub-mesh data and rendering
- **ShdLegacyW3DDefClass (Class)**: Legacy shader definition for W3D compatibility
- **Shd6LegacyW3DClass (Class)**: Legacy shader implementation
- **W3dShdSubMeshHeaderStruct (Struct)**: Header structure for W3D sub-mesh data

## Key Functions
### `Define_FVF(MeshModelClass*, bool)`
- Purpose: Determines the Flexible Vertex Format for legacy mesh rendering
- Calls: `Get_Flag`, `Get_UV_Array_Count`, `Get_Color_Array`, `Needs_Vertex_Normals`

### `Define_FVF(ShdSubMeshClass*, bool)`
- Purpose: Determines the Flexible Vertex Format for shader-based sub-mesh rendering
- Calls: `Get_Flag`, `Get_UV_Array`, `Get_Diffuse_Array`, `Get_Vertex_Normal_Array`

### `Init_From_Legacy_Mesh_Model(MeshModelClass*, int)`
- Purpose: Converts legacy mesh data to shader-based sub-mesh format
- Calls: `NEW_REF`, `REF_PTR_SET`, `REF_PTR_RELEASE`, `Set_FVF`, `Set_Pass_Count`, `Set_Texture`, `Set_Shader`, `Set_Material`

### `Load_W3D(ChunkLoadClass&)`
- Purpose: Loads sub-mesh data from W3D file format
- Calls: `Open_Chunk`, `Read`, `Close_Chunk`, `NEW_REF`, `Clear`, `read_vertex_normals`, `read_uv0`, `read_uv1`, etc.

### `Get_Deformed_Vertices(Vector3*, Vector3*, const HTreeClass*)`
- Purpose: Retrieves deformed vertex data for skinned meshes
- Calls: `get_deformed_vertices`

## Globals
- **None**

## Dependencies
- Key includes: `shddefmanager.h`, `shdsubmesh.h`, `shdrenderer.h`, `shdlegacyw3d.h`, `shdclassids.h`, `chunkio.h`, `texture.h`, `w3d_file.h`, `ww3d.h`, `dx8fvf.h`, `dx8wrapper.h`, `meshmdl.h`, `aabtree.h`, `sharebuf.h`
- External symbols: `WW3D::Is_Sorting_Enabled()`, `ShdDefManagerClass::Load_Shader()`, `MeshGeometryClass` methods, `Vector2`, `Vector3`, `TriIndex`, `ShareBufferClass`, `HTreeClass`
