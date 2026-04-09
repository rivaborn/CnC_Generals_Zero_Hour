# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdsubmesh.h

## Purpose
Defines the `ShdSubMeshClass`, representing a sub-mesh with shared shader properties in the W3D rendering system.

## Responsibilities
- Manages vertex data, UV coordinates, and tangent basis for rendering
- Handles shader assignment and decal generation
- Loads W3D mesh data and provides access to vertex attributes
- Supports visibility culling and vertex deformation for skinned meshes

## Key Types
- **ShdSubMeshClass (Class)**: Sub-mesh with shared shader, containing vertices, UVs, and tangent data
- **DecalGeneratorClass (Class)**: External decal generation interface
- **ShdInterfaceClass (Class)**: Shader interface reference
- **RenderInfoClass (Class)**: Rendering context (forward declared)
- **MeshModelClass (Class)**: Legacy mesh model (forward declared)
- **HTreeClass (Class)**: Hierarchy tree for skinned mesh deformation (forward declared)

## Key Functions
### `Set_Shader`
- Purpose: Assigns a shader to the sub-mesh
- Calls: `REF_PTR_SET`

### `Load_W3D`
- Purpose: Loads sub-mesh data from a W3D chunk file
- Calls: `read_chunks`, `read_vertices`, etc.

### `Get_Deformed_Vertices`
- Purpose: Computes deformed vertices for skinned meshes
- Calls: Not inferable (implementation in .cpp)

### `read_chunks`
- Purpose: Parses W3D chunk data during loading
- Calls: Not inferable (implementation in .cpp)

## Globals
- **UV[MAX_TEXTURE_STAGES] (ShareBufferClass<Vector2>*)**: UV coordinate arrays per texture stage
- **Diffuse (ShareBufferClass
