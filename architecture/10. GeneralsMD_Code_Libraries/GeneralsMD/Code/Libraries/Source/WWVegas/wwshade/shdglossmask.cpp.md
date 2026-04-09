# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdglossmask.cpp

## Purpose
Implements a gloss mask shader effect for the SAGE engine, handling texture loading, material properties, and DirectX rendering states.

## Responsibilities
- Defines `ShdGlossMaskDefClass` for shader configuration (textures, colors)
- Implements `Shd6GlossMaskClass` for runtime shader application
- Manages DirectX texture stages and material states
- Handles vertex stream formatting for rendering
- Provides save/load persistence for shader parameters

## Key Types
- `ShdGlossMaskDefClass` (Class): Shader definition with texture and color parameters
- `Shd6GlossMaskClass` (Class): Runtime shader implementation for DirectX 6
- `CHUNKID_VARIABLES` (Enum): Chunk ID for save/load operations
- `VARID_TEXTURE_NAME` (Enum): Variable ID for texture name
- `VARID_AMBIENT_COLOR` (Enum): Variable ID for ambient color
- `VARID_DIFFUSE_COLOR` (Enum): Variable ID for diffuse color
- `VARID_SPECULAR_COLOR` (Enum): Variable ID for specular color

## Key Functions
### `Apply_Shared`
- Purpose: Sets up shared DirectX rendering states for the gloss mask effect
- Calls: `DX8Wrapper::Set_DX8_Texture_Stage_State`, `DX8Wrapper::Set_Vertex_Shader`, `DX8Wrapper::Set_DX8_Render_State`, `DX8Wrapper::Set_DX8_Material`

### `Apply_Instance`
- Purpose: Applies per-instance DirectX states (textures, materials)
- Calls: `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_DX8_Material`

### `Copy_Vertex_Stream`
- Purpose: Formats vertex data for rendering with position, normal, diffuse, and UV attributes
- Calls: None (direct vertex buffer manipulation)

## Globals
- `View_Projection_Matrix` (Matrix4x4): Static matrix for view/projection transformations

## Dependencies
- DirectX 8 headers (`d3dx8math.h`, `dx8fvf.h`, `dx8wrapper.h`)
- Engine systems (`assetmgr.h`, `shdinterface.h`, `shdhwshader.h`)
- Persistence framework (`persistfactory.h`, `wwhack.h`)
- Shader definition system (`shdclassids.h`, `shddeffactory.h`)
