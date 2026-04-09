# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshmatdesc.h

## Purpose
Defines material description classes for 3D meshes, including UV coordinates, textures, shaders, and vertex materials.

## Responsibilities
- Manages mesh material data (textures, shaders, vertex materials)
- Handles UV coordinate arrays and color arrays
- Provides accessors for material properties
- Supports per-polygon and per-vertex material arrays
- Handles reference counting for shared resources

## Key Types
- **MeshMatDescClass (Class)**: Encapsulates material description data for a mesh
- **MatBufferClass (Class)**: ShareBufferClass for VertexMaterialClass pointers
- **TexBufferClass (Class)**: ShareBufferClass for TextureClass pointers
- **UVBufferClass (Class)**: ShareBufferClass for Vector2 UV coordinates with CRC
- **(anonymous enum) (Enum)**: Defines MAX_PASSES, MAX_TEX_STAGES, MAX_COLOR_ARRAYS, MAX_UV_ARRAYS

## Key Functions
### `MeshMatDescClass::Get_UV_Array`
- Purpose: Retrieves UV array for a specific pass and texture stage
- Calls: None

### `MeshMatDescClass::Set_UV_Source`
- Purpose: Sets UV source index for a pass and texture stage
- Calls: None

### `MeshMatDescClass::Get_DCG_Array`
- Purpose: Gets diffuse color array based on source type
- Calls: None

### `MeshMatDescClass::Post_Load_Process`
- Purpose: Configures materials after loading
- Calls: `Configure_Material`, `Disable_Backface_Culling`

### `UVBufferClass::Update_CRC`
- Purpose: Updates CRC for UV buffer equality checking
- Calls: None

## Globals
- **MeshMatDescClass::NullShader (ShaderClass)**: Marker for no shader data

## Dependencies
- `always.h`, `vector2.h`, `vector3.h`, `vector3i.h`, `vector4.h`, `sharebuf.h`, `shader.h`, `vertmaterial.h`
- `W3DMPO`, `ShareBufferClass`, `VertexMaterialClass`, `TextureClass`, `ShaderClass`
