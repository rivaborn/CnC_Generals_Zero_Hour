# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpspec.cpp

## Purpose
Implements DirectX 8 bump-mapping and specular shading for the SAGE engine.

## Responsibilities
- Manages vertex and pixel shaders for bump/specular effects
- Handles texture and normal map loading
- Sets up shader constants and matrices
- Implements self-shadowing via shadow maps

## Key Types
- `Shd8BumpSpecClass` (Class): Main shader implementation for bump/specular rendering
- `ShdHWVertexShader` (Class): Vertex shader wrapper
- `ShdHWPixelShader` (Class): Pixel shader wrapper

## Key Functions
### `Init`
- Purpose: Initializes vertex and pixel shaders
- Calls: `Create` on shader objects

### `Apply_Shared`
- Purpose: Sets up shared shader state
- Calls: `DX8Wrapper::Set_Vertex_Shader`, `DX8Wrapper::Set_Pixel_Shader`

### `Apply_Instance`
- Purpose: Applies per-instance shader parameters
- Calls: `DX8Wrapper::Set_Texture`, `ShdHWVertexShader::Light`

### `Setup_Self_Shadow_Info`
- Purpose: Configures shadow map transform
- Calls: `DX8Wrapper::Get_Shadow_Map`, `Matrix4x4::Multiply`

## Globals
- `Vertex_Shader` (ShdHWVertexShader): Main vertex shader
- `Pixel_Shader` (ShdHWPixelShader): Main pixel shader
- `Self_Shadow_Pixel_Shader` (ShdHWPixelShader): Self-shadow pixel shader
- `Self_Shadow_Vertex_Shader` (ShdHWVertexShader): Self-shadow vertex shader
- `View_Projection_Matrix` (Matrix4x4): Combined view/projection matrix

## Dependencies
- `dx8fvf.h`, `dx8wrapper.h`, `assetmgr.h`, `rinfo.h`, `camera.h`, `shdmesh.h`, `texproject.h`
- `shdbumpspec.h`, `shd8bumpspec.h`, `shd8bumpspec_constants.h`, `shdclassids.h`
- Shader code headers (`shd8bumpspec.vsh_code.h`, etc.)
