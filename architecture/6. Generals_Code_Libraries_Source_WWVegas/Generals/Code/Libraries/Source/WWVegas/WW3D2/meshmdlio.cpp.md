# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshmdlio.cpp

## Purpose
Handles loading and saving of 3D mesh models in the W3D format for the SAGE engine.

## Responsibilities
- Implements mesh loading from W3D files via `MeshModelClass::Load_W3D`
- Manages temporary loading context with `MeshLoadContextClass`
- Handles mesh saving with `MeshSaveContextClass`
- Processes various mesh chunks (vertices, materials, textures, etc.)

## Key Types
- **MeshLoadContextClass (Class)**: Temporary scratchpad during mesh loading, holds material references
- **LegacyMaterialClass (Class)**: Stores legacy material references (shader, vertex material, texture)
- **MeshSaveContextClass (Class)**: Context for mesh saving operations

## Key Functions
### MeshModelClass::Load_W3D
- Purpose: Load a mesh from a W3D file
- Calls: `read_chunks`, `Reset`, `Set_Name`, `read_vertices`, `read_texcoords`, etc.

### MeshLoadContextClass::Add_Shader
- Purpose: Add a shader to the context's shader array
- Calls: Not inferable

### MeshModelClass::write_vertices
- Purpose: Write vertex data to a W3D file
- Calls: `csave.Begin_Chunk`, `csave.Write`, `csave.End_Chunk`

### MeshModelClass::write_material_info
- Purpose: Write material information chunk
- Calls: `csave.Begin_Chunk`, `csave.Write`, `csave.End_Chunk`

## Globals
- `W3dAttributes (uint32)`: Stores mesh attributes from header
- `SortLevel (int)`: Mesh sort level from header

## Dependencies
- Key includes: `meshmdl.h`, `aabtree.h`, `matinfo.h`, `vertmaterial.h`, `shader.h`, `texture.h`, `chunkio.h`
- External symbols: `W3DNEW`, `WWDEBUG_SAY`, `W3DMPO_GLUE`, `DynamicVectorClass`, `Vector3`, `Vector2`
