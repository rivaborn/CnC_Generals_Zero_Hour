# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpdiff.cpp

## Purpose
Implements a DirectX 8 bump-diffuse shader for rendering meshes with normal mapping and self-shadowing effects.

## Responsibilities
- Manages vertex and pixel shaders for bump-diffuse rendering
- Handles texture and normal map loading
- Sets up shader constants and matrices for rendering
- Implements self-shadow mapping logic
- Provides vertex stream formatting for the shader

## Key Types
- `Shd8BumpDiffClass` (Class): Main shader implementation handling bump-diffuse rendering
- `VertexFormatXYZNDUV1TG3` (Struct): Vertex format for the shader (not shown in file but used)
- `ShdHWVertexShader`/`ShdHWPixelShader` (Classes): Shader wrapper classes

## Key Functions
### `Init`
- Purpose: Initializes vertex and pixel shaders for the bump-diffuse effect
- Calls: `Create` on shader objects

### `Apply_Shared`
- Purpose: Sets up shared shader state for all passes
- Calls: `DX8Wrapper::Set_Vertex_Shader`, `DX8Wrapper::Set_Pixel_Shader`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `DX8Wrapper::Get_Transform`, `Matrix4x4::Multiply`

### `Apply_Instance`
- Purpose: Applies per-instance shader state including textures and matrices
- Calls: `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Vertex_Shader_Constant`, `DX8Wrapper::Get_Transform`, `Matrix4x4::Multiply`, `ShdHWVertexShader::Light`

### `Setup_Self_Shadow_Info`
- Purpose: Calculates self-shadow transformation matrix
- Calls: `Peek_Texture_Projector`, `Peek_Mapper`, `Get_Texture_Transform`, `DX8Wrapper::Get_Shadow_Map`, `Matrix4x4::Multiply`, `Get_Num_Depth_Bits`

## Globals
- `Vertex_Shader`/`Pixel_Shader`/`Self_Shadow_Pixel_Shader`/`Self_Shadow_Vertex_Shader` (ShdHWVertexShader/ShdHWPixelShader): Static shader objects
- `View_Projection_Matrix` (Matrix4x4): Cached view-projection matrix
- `Self_Shadow_Transform` (Matrix4x4): Self-shadow transformation matrix

## Dependencies
- DirectX 8 headers (`dx8fvf.h`, `dx8wrapper.h`)
- Game engine headers (`assetmgr.h`, `rinfo.h`, `camera.h`, `shdmesh.h`, `texproject.h`)
