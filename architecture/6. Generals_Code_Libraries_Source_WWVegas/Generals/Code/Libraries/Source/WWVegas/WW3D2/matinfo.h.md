# Generals/Code/Libraries/Source/WWVegas/WW3D2/matinfo.h

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
### MaterialInfoClass::Add_Vertex_Material
- Purpose: Adds a vertex material to the collection and increments its reference count
- Calls: VertexMaterialClass::Add_Ref()

### MaterialInfoClass::Get_Vertex_Material_Index
- Purpose: Finds the index of a vertex material by name
- Calls: VertexMaterialClass::Get_Name()

### MaterialInfoClass::Replace_Material
- Purpose: Replaces a vertex material at a specific index
- Calls: REF_PTR_SET()

### MaterialRemapperClass::Remap_Texture
- Purpose: Remaps a texture pointer from source to destination material info
- Calls: Not inferable

### MaterialCollectorClass::Collect_Materials
- Purpose: Collects all unique materials from a mesh model
- Calls: Not inferable

## Globals
None

## Dependencies
- "always.h", "wwdebug.h", "vector.h", "vertmaterial.h", "texture.h", "shader.h"
- MeshModelClass, MeshMatDescClass (forward declarations)
- VertexMaterialClass, TextureClass, ShaderClass (external types)
- DynamicVectorClass, RefCountClass, W3DMPO (base classes)
