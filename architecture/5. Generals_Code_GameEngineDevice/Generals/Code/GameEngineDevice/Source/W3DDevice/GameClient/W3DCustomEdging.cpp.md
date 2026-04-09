# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DCustomEdging.cpp

## Purpose
Handles rendering of custom tile edges in a 3D scene using vertex/index buffers and shaders.

## Responsibilities
- Manages vertex/index buffers for edge geometry
- Loads edge data into buffers based on terrain blend tiles
- Renders edges with alpha testing and texturing
- Supports multiple texture layers (terrain, cloud, noise)

## Key Types
- **W3DCustomEdging (Class)**: Main class managing custom edge rendering
- **ShaderClass (Static)**: Predefined shaders for alpha testing and blending
- **VertexFormatXYZDUV2**: Vertex format for edge geometry

## Key Functions
### `loadEdgingsInVertexAndIndexBuffers`
- Purpose: Loads edge geometry into vertex/index buffers based on terrain blend tiles
- Calls: `DX8IndexBufferClass::WriteLockClass`, `DX8VertexBufferClass::WriteLockClass`, `WorldHeightMap::getUVForBlend`, `WorldHeightMap::getAlphaUVData`

### `drawEdging`
- Purpose: Renders custom edges with multiple texture passes
- Calls: `DX8Wrapper::Set_*`, `DX8Wrapper::Draw_Triangles`, `loadEdgingsInVertexAndIndexBuffers`

### `allocateEdgingBuffers`
- Purpose: Allocates vertex and index buffers for edge geometry
- Calls: `NEW_REF`

### `freeEdgingBuffers`
- Purpose: Releases vertex and index buffers
- Calls: `REF_PTR_RELEASE`

## Globals
- **detailAlphaTestShader (ShaderClass)**: Shader for alpha-tested edge rendering
- **detailShader (ShaderClass)**: Shader for non-alpha edge rendering
- **detailOpaqueShader (ShaderClass)**: Shader for opaque edge rendering

## Dependencies
- Key includes: `W3DCustomEdging.h`, `DX8Wrapper.h`, `DX8Renderer.h`, `Mesh.h`, `TerrainTex.h`, `HeightMap.h`
- External symbols: `DX8VertexBufferClass`, `DX8IndexBufferClass`, `ShaderClass`, `TextureClass`, `WorldHeightMap`
