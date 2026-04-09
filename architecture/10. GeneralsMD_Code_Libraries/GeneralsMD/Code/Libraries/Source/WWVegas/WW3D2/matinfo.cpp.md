# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matinfo.cpp

## Purpose
Manages material and texture information for 3D models in the SAGE engine, including cloning, remapping, and collecting materials.

## Responsibilities
- Manages `MaterialInfoClass` for storing vertex materials and textures
- Provides material remapping functionality via `MaterialRemapperClass`
- Collects materials from mesh models via `MaterialCollectorClass`
- Handles reference counting for textures and materials

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
- Purpose: Remaps materials/textures in a mesh description
- Calls: `Remap_Vertex_Material`, `Remap_Texture`

### `MaterialCollectorClass::Collect_Materials`
- Purpose: Gathers materials from a mesh model
- Calls: `Add_Vertex_Material`, `Add_Shader`, `Add_Texture`

## Globals
None

## Dependencies
- `matinfo.h`, `wwdebug.h`, `meshmdl.h`, `texture.h`
- `MaterialInfoClass`, `VertexMaterialClass`, `TextureClass`, `MeshModelClass`, `MeshMatDescClass`
