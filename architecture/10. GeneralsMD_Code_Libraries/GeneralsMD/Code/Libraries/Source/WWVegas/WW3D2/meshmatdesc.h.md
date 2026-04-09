# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshmatdesc.h

## Purpose
Defines classes for managing mesh material descriptions, including textures, shaders, UV coordinates, and vertex colors in the SAGE engine.

## Responsibilities
- Encapsulates material data for 3D meshes (textures, shaders, UVs, colors)
- Manages per-polygon/per-vertex material arrays
- Provides accessors for material properties
- Handles reference counting for shared resources
- Supports alternate material descriptions

## Key Types
- **MeshMatDescClass (Class)**: Main class for mesh material descriptions
- **MatBufferClass (Class)**: ShareBuffer for VertexMaterialClass pointers
- **TexBufferClass (Class)**: ShareBuffer for TextureClass pointers
- **UVBufferClass (Class)**: ShareBuffer for Vector2 UV coordinates with CRC
- **(anonymous enum) (Enum)**: Defines MAX_PASSES, MAX_TEX_STAGES, MAX_COLOR_ARRAYS, MAX_UV_ARRAYS

## Key Functions
### `MeshMatDescClass::Reset`
- Purpose: Initializes material description with given poly/vertex/pass counts
- Calls: None

### `MeshMatDescClass::Post_Load_Process`
- Purpose: Configures materials after loading (lighting, passes, etc.)
- Calls: `Configure_Material`, `Disable_Backface_Culling`

### `UVBufferClass::Update_CRC`
- Purpose: Computes CRC for UV array comparison
- Calls: None

## Globals
- **NullShader (ShaderClass)**: Marker for no shader data

## Dependencies
- `vector2.h`, `vector3.h`, `vector3i.h`, `vector4.h`
- `sharebuf.h`, `shader.h`, `vertmaterial.h`
- `W3DMPO` (memory management)
- `VertexMaterialClass`, `TextureClass`, `MeshModelClass` (forward declarations)
