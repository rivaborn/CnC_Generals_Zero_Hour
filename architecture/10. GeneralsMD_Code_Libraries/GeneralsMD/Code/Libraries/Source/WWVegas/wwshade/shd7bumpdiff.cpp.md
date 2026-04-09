# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpdiff.cpp

## Purpose
Implements a DirectX 7-style bump-mapping shader for the SAGE engine, handling two-pass rendering with normal mapping and diffuse lighting.

## Responsibilities
- Manages vertex shaders for bump-diffuse rendering
- Configures texture stages and render states for two-pass shading
- Handles vertex stream formatting for bump-mapping
- Sets up lighting and material constants for the shader

## Key Types
- **Shd7BumpDiffClass (Class)**: Main shader implementation for DX7 bump-diffuse effect
- **VertexFormatXYZNDUV1TG3 (Struct)**: Vertex format containing position, normal, color, UVs, and tangent space vectors

## Key Functions
### `Init`
- Purpose: Initializes vertex shaders and their declarations
- Calls: `ShdHWVertexShader::Create`

### `Apply_Shared`
- Purpose: Sets up shared render states for both passes
- Calls: `DX8Wrapper::Set_DX8_Render_State`, `DX8Wrapper::Set_DX8_Texture_Stage_State`, `DX8Wrapper::Set_Vertex_Shader`

### `Apply_Instance`
- Purpose: Configures per-instance shader constants and textures
- Calls: `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `ShdHWVertexShader::Light`

### `Copy_Vertex_Stream`
- Purpose: Formats vertex data for bump-mapping
- Calls: None (direct vertex data copying)

## Globals
- **Pass_0_Vertex_Shader (ShdHWVertexShader)**: Vertex shader for first pass
- **Pass_1_Vertex_Shader (ShdHWVertexShader)**: Vertex shader for second pass
- **View_Projection_Matrix (Matrix4x4)**: Combined view-projection matrix

## Dependencies
- `dx8fvf.h`, `dx8wrapper.h`, `assetmgr.h`, `rinfo.h`, `camera.h`, `shdhwshader.h`
- `shdbumpdiff.h`, `shd7bumpdiff.h`, `shd7bumpdiff_constants.h`, `shdclassids.h`
- `shd7bumpdiffpass0.vsh_code.h`, `shd7bumpdiffpass1.vsh_code.h`
