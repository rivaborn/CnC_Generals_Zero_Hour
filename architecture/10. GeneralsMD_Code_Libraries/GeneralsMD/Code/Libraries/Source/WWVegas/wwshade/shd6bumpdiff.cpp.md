# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpdiff.cpp

## Purpose
Implements a DirectX 6 bump-diffuse shader for the SAGE engine, handling vertex shaders and rendering states.

## Responsibilities
- Manages vertex shader creation and destruction
- Applies shared and per-instance rendering states
- Handles vertex stream formatting for rendering
- Sets up texture and lighting for shader passes

## Key Types
- **Shd6BumpDiffClass (Class)**: Main shader implementation for bump-diffuse effects
- **ShdHWVertexShader (Type)**: Hardware vertex shader wrapper
- **Matrix4x4 (Type)**: 4x4 transformation matrix
- **VertexFormatXYZNDUV1 (Struct)**: Vertex format with position, normal, diffuse, and UV data

## Key Functions
### `Init`
- Purpose: Initializes the vertex shader and its declaration
- Calls: `Vertex_Shader.Create`

### `Shutdown`
- Purpose: Cleans up the vertex shader
- Calls: `Vertex_Shader.Destroy`

### `Apply_Shared`
- Purpose: Sets up shared rendering states for shader passes
- Calls: `DX8Wrapper::Set_DX8_Render_State`, `DX8Wrapper::Set_DX8_Texture_Stage_State`, `DX8Wrapper::Set_Vertex_Shader`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `DX8Wrapper::Get_Transform`, `Matrix4x4::Multiply`

### `Apply_Instance`
- Purpose: Configures per-instance rendering states
- Calls: `DX8Wrapper::Set_Texture`, `DX8Wrapper::Get_Transform`, `Matrix4x4::Multiply`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `ShdHWVertexShader::Light`

### `Copy_Vertex_Stream`
- Purpose: Formats vertex data for rendering
- Calls: None (direct vertex data manipulation)

## Globals
- **Vertex_Shader (ShdHWVertexShader)**: Static vertex shader instance
- **View_Projection_Matrix (Matrix4x4)**: Static matrix for view-projection transformations

## Dependencies
- Key includes: `dx8fvf.h`, `dx8wrapper.h`, `assetmgr.h`, `rinfo.h`, `camera.h`, `shdbumpdiff.h`, `shd6bumpdiff.h`, `shd6bumpdiff_constants.h`, `shdclassids.h`, `shd6bumpdiff.vsh_code.h`
- External symbols: `D3DVSD_STREAM`, `D3DVSD_REG`, `D3DVSDT_FLOAT3`, `D3DVSDT_D3DCOLOR`, `D
