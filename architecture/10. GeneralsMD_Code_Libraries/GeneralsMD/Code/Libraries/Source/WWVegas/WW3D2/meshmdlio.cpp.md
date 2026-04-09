# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshmdlio.cpp

## Purpose
Handles loading and saving of 3D mesh models in the W3D format, including vertex data, materials, textures, and rendering attributes.

## Responsibilities
- Load W3D mesh files with vertices, normals, textures, materials, and shaders
- Save mesh data to W3D format
- Manage material and texture references during load/save
- Handle legacy material formats and conversions
- Process chunk-based W3D file structure

## Key Types
- **MeshLoadContextClass (Class)**: Temporary scratchpad for mesh loading, holding material references and conversion state
- **LegacyMaterialClass (Class)**: Stores legacy material references (shader, vertex material, texture indices)
- **MeshSaveContextClass (Class)**: Context for mesh saving operations, tracking current pass/stage and material collection

## Key Functions
### MeshModelClass::Load_W3D
- Purpose: Load a mesh from a W3D file
- Calls: read_chunks, various read_* functions, W3DNEW, W3DNEWARRAY

### MeshModelClass::Save
- Purpose: Save mesh model to W3D format
- Calls: write_vertices, write_vertex_normals, write_triangles, write_material_info, etc.

### MeshLoadContextClass::Add_Shader
- Purpose: Add a shader to the context's shader array
- Calls: Shaders.Add

### MeshLoadContextClass::Add_Vertex_Material
- Purpose: Add a vertex material to the context
- Calls: VertexMaterials.Add, VertexMaterialCrcs.Add

### MeshLoadContextClass::Add_Texture
- Purpose: Add a texture to the context
- Calls: Textures.Add

## Globals
- **W3dAttributes (uint32)**: Mesh attribute flags
- **SortLevel (int)**: Mesh sorting level
- **BoundBoxMin/Max (Vector3)**: Mesh bounding box
- **BoundSphereCenter (Vector3)**: Mesh bounding sphere center
- **BoundSphereRadius (float)**: Mesh bounding sphere radius

## Dependencies
- meshmdl.h, aabtree.h, matinfo.h, vertmaterial.h, shader.h, texture.h, chunkio.h, w3derr.h, w3d_file.h, w3d_util.h, assetmgr.h, simplevec.h, realcrc.h, dx8wrapper.h
- W3DMPO (memory pool base class)
- DynamicVectorClass, StringClass, Vector2/3/4 classes
- ChunkLoadClass, ChunkSaveClass for file I/O
