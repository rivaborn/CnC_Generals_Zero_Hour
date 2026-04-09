# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdmesh.h

## Purpose
Defines the `ShdMeshClass`, a render object for shaded meshes in the SAGE engine, supporting sub-meshes, lighting, and collision detection.

## Responsibilities
- Manages shaded mesh rendering with sub-meshes
- Handles collision detection and bounding volumes
- Supports lighting environments and texture projection
- Loads W3D mesh data and generates culling trees

## Key Types
- **ShdMeshClass (Class)**: Main shaded mesh class, extends `RenderObjClass`.
- **ShdSubMeshStruct (Struct)**: Contains a sub-mesh and its renderer.
- **ChunkLoadClass (Class)**: Forward declaration for chunk loading.
- **LightEnvironmentClass (Class)**: Forward declaration for lighting.
- **MaterialPassClass (Class)**: Forward declaration for material passes.
- **ShdSubMeshClass (Class)**: Forward declaration for sub-mesh handling.
- **ShdRendererNodeClass (Class)**: Forward declaration for renderer nodes.
- **MeshClass (Class)**: Forward declaration for legacy mesh compatibility.
- **TexProjectClass (Class)**: Forward declaration for texture projection.

## Key Functions
### `ShdMeshClass::Render`
- Purpose: Renders the mesh with given render info.
- Calls: Not inferable (implementation in .cpp).

### `ShdMeshClass::Load_W3D`
- Purpose: Loads mesh data from a W3D chunk.
- Calls: `ChunkLoadClass` methods (not inferable).

### `ShdMeshClass::Generate_Culling_Tree`
- Purpose: Generates a culling tree for optimization.
- Calls: Not inferable.

### `ShdMeshClass::Get_Deformed_Vertices`
- Purpose: Retrieves deformed vertex data (with/without normals).
-
