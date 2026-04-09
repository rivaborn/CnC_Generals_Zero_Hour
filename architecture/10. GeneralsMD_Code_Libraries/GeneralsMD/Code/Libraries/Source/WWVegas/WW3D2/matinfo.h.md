# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matinfo.h

## Purpose
Defines classes for managing material information in W3D render objects, including textures and vertex materials.

## Responsibilities
- Manage material references for meshes
- Provide remapping functionality for material pointers
- Collect unique material instances from meshes
- Handle texture and vertex material operations

## Key Types
- **MaterialInfoClass (Class)**: Interface for changeable material parameters in W3D render objects
- **MaterialRemapperClass (Class)**: Remaps material pointers between source and destination material info objects
- **MaterialCollectorClass (Class)**: Collects unique material instances from meshes
- **VmatRemapStruct (Struct)**: Stores source/destination vertex material pairs for remapping
- **TextureRemapStruct (Struct)**: Stores source/destination texture pairs for remapping

## Key Functions
### `Add_Vertex_Material`
- Purpose: Adds a vertex material to the material info and increments its reference count
- Calls: `Add_Ref()`

### `Get_Vertex_Material_Index`
- Purpose: Finds the index of a vertex material by name
- Calls: `stricmp()`

### `Get_Vertex_Material`
- Purpose: Retrieves a vertex material by index with reference counting
- Calls: `Add_Ref()`

### `Replace_Material`
- Purpose: Replaces a vertex material at a specific index
- Calls: `REF_PTR_SET()`

### `Reset_Texture_Mappers`
- Purpose: Resets texture mappers for all vertex materials
- Calls: `Reset_Mappers()`

### `Remap_Texture`
- Purpose: Remaps a texture pointer from source to destination material info
- Calls: None visible

### `Remap_Vertex_Material`
- Purpose: Remaps a vertex material pointer from source to destination material info
- Calls: None visible

### `Collect_Materials`
- Purpose: Collects unique materials from a mesh into the collector
- Calls: `Add_Texture()`, `Add_Shader()`, `Add_Vertex_Material()`

## Globals
- None

## Dependencies
- `always.h`, `wwdebug.h`, `vector.h`, `vertmaterial.h`, `texture.h`, `shader.h`
- `MeshModelClass`, `MeshMatDescClass` (forward declarations)
- `RefCountClass`, `W3DMPO`, `DynamicVectorClass`, `VertexMaterialClass`, `TextureClass`, `ShaderClass`
