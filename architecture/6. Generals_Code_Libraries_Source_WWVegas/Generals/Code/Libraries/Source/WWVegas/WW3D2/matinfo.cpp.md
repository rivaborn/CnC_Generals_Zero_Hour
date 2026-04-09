# Generals/Code/Libraries/Source/WWVegas/WW3D2/matinfo.cpp

## Purpose
Manages material and texture information for 3D models in the SAGE engine, including collection, remapping, and reference counting.

## Responsibilities
- Manages `MaterialInfoClass` for storing vertex materials and textures
- Provides `MaterialRemapperClass` for remapping materials/textures between models
- Implements `MaterialCollectorClass` to gather materials from mesh models
- Handles reference counting and memory management for materials/textures
- Supports cloning and serialization of material data

## Key Types
- **MaterialInfoClass (Class)**: Stores vertex materials and textures for a model
- **MaterialRemapperClass (Class)**: Remaps materials/textures between source and destination models
- **MaterialCollectorClass (Class)**: Collects materials from mesh models
- **VmatRemapStruct (Struct)**: Maps source/destination vertex materials
- **TextureRemapStruct (Struct)**: Maps source/destination textures

## Key Functions
### `MaterialInfoClass::Clone`
- Purpose: Creates a deep copy of the material info
- Calls: Constructor

### `MaterialRemapperClass::Remap_Mesh`
- Purpose: Remaps materials/textures from source to destination mesh
- Calls: `Remap_Vertex_Material`, `Remap_Texture`, `Set_Material`, `Set_Texture`

### `MaterialCollectorClass::Collect_Materials`
- Purpose: Gathers all materials from a mesh model
- Calls: `Add_Vertex_Material`, `Add_Shader`, `Add_Texture`

## Globals
None

## Dependencies
- `matinfo.h` (header)
- `wwdebug.h` (assertions)
- `meshmdl.h` (mesh model)
- `texture.h` (texture)
- `VertexMaterialClass`, `TextureClass`, `MeshMatDescClass`, `ShaderClass` (external types)
