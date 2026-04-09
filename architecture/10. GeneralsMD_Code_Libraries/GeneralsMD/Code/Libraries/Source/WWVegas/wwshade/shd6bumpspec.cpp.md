# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpspec.cpp

## Purpose
Implements a DirectX 6 bump-specular shader for rendering materials with gloss maps.

## Responsibilities
- Manages vertex shader creation and destruction
- Applies shared and per-instance render states
- Handles texture loading and shader constant setup
- Provides vertex stream formatting for rendering

## Key Types
- **Shd6BumpSpecClass (Class)**: Main shader implementation for bump-specular effects
- **ShdHWVertexShader (Class)**: Vertex shader wrapper
- **VertexFormatXYZNDUV1 (Struct)**: Vertex format definition

## Key Functions
### `Init`
- Purpose: Initializes the vertex shader and its declaration
- Calls: `Vertex_Shader.Create`

### `Apply_Shared`
- Purpose: Sets up shared render states for the shader pass
- Calls: `DX8Wrapper::Set_DX8_Render_State`, `DX8Wrapper::Set_DX8_Texture_Stage_State`, `DX8Wrapper::Set_Vertex_Shader`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `Matrix4x4::Multiply`

### `Apply_Instance`
- Purpose: Applies per-instance render states and shader constants
- Calls: `DX8Wrapper::Set_Texture`, `DX8Wrapper::Get_Transform`, `Matrix4x4::Multiply`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `ShdHWVertexShader::Light`

### `Copy_Vertex_Stream`
- Purpose: Formats vertex data for rendering
- Calls: None (direct vertex data manipulation)

## Globals
- **Vertex_Shader (ShdHWVertexShader)**: Static vertex shader instance
- **View_Projection_Matrix (Matrix4x4)**: Static matrix for view-projection transformations

## Dependencies
- `dx8fvf.h`, `dx8wrapper.h`, `assetmgr.h`, `rinfo.h`, `camera.h`
- `shdbumpspec.h`, `shd6bumpspec.h`, `shd6bumpspec_constants.h`, `shdclassids.h`
- `shd6bumpspec.vsh_code.h` (shader code)
- DirectX 8 SDK symbols (`D3DVSD_*`, `D3DTSS_*`, `D3DTOP_*`, etc.)
