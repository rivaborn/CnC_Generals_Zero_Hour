# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matpass.cpp

## Purpose
Manages material passes for rendering, including textures, shaders, and vertex materials in the SAGE engine.

## Responsibilities
- Encapsulates material pass state (textures, shaders, materials)
- Handles reference counting for textures and materials
- Installs material settings into Direct3D via DX8Wrapper
- Manages per-polygon culling and translucency flags

## Key Types
- **MaterialPassClass (Class)**: Core class managing material passes for rendering.
- **VertexMaterialClass (Class)**: Vertex material reference (external).
- **ShaderClass (Class)**: Shader reference (external).
- **TextureClass (Class)**: Texture reference (external).

## Key Functions
### `Install_Materials`
- Purpose: Applies material settings to Direct3D.
- Calls: `DX8Wrapper::Set_Material`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Set_Texture`, `Peek_Material`, `Peek_Shader`, `Peek_Texture`.

### `Set_Texture`
- Purpose: Assigns a texture to a specific stage.
- Calls: `REF_PTR_SET`.

### `Set_Shader`
- Purpose: Sets the shader for this material pass.
- Calls: `Shader.Enable_Fog`.

### `Set_Material`
- Purpose: Assigns a vertex material to this pass.
- Calls: `REF_PTR_SET`.

### `Get_Texture`
- Purpose: Retrieves a reference-counted texture pointer.
- Calls: `Add_Ref`.

### `Get_Material`
- Purpose: Retrieves a reference-counted vertex material pointer.
- Calls: `Add_Ref`.

## Globals
- **EnablePerPolygonCulling (bool)**: Controls per-polygon culling behavior.

## Dependencies
- `matpass.h`, `vertmaterial.h`, `shader.h`, `texture.h`, `statistics.h`, `dx8wrapper.h`
- `DX8Wrapper`, `ShaderClass`, `VertexMaterialClass`, `TextureClass`, `REF_PTR_SET/RELEASE`
