# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpspec.cpp

## Purpose
Implements a DirectX 7-compatible bump specular shader with gloss mapping for the SAGE engine.

## Responsibilities
- Manages vertex shaders for bump specular rendering
- Handles texture and material state setup
- Provides vertex stream formatting for rendering
- Configures render states for two-pass bump specular effect

## Key Types
- `Shd7BumpSpecClass` (Class): Main shader implementation for DX7 bump specular
- `ShdHWVertexShader` (Class): Hardware vertex shader wrapper
- `VertexFormatXYZNDUV1TG3` (Struct): Vertex format for bump specular rendering

## Key Functions
### `Init`
- Purpose: Initializes vertex shaders and their declarations
- Calls: `Pass_0_Vertex_Shader.Create`, `Pass_1_Vertex_Shader.Create`

### `Apply_Shared`
- Purpose: Sets up shared render states for both shader passes
- Calls: `DX8Wrapper::Set_DX8_Render_State`, `DX8Wrapper::Set_DX8_Texture_Stage_State`, `DX8Wrapper::Set_Vertex_Shader`

### `Apply_Instance`
- Purpose: Configures per-instance shader parameters
- Calls: `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `ShdHWVertexShader::Light`

### `Copy_Vertex_Stream`
- Purpose: Formats vertex data for bump specular rendering
- Calls: None (direct vertex data manipulation)

## Globals
- `Pass_0_Vertex_Shader` (ShdHWVertexShader): First pass vertex shader
- `Pass_1_Vertex_Shader` (ShdHWVertexShader): Second pass vertex shader
- `View_Projection_Matrix` (Matrix4x4): Combined view/projection matrix

## Dependencies
- `dx8fvf.h`, `dx8wrapper.h`, `assetmgr.h`, `rinfo.h`, `camera.h`
- `shdbumpspec.h`, `shd7bumpspec.h`, `shd7bumpspec_constants.h`, `shdclassids.h`
- `shd7bumpspecpass0.vsh_code.h`, `shd7bumpspecpass1.vsh_code.h`
