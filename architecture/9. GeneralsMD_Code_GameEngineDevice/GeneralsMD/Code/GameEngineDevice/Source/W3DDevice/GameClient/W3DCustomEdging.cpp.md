# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DCustomEdging.cpp

## Purpose
Handles rendering of custom tile edges in a 3D scene using vertex/index buffers and shaders.

## Responsibilities
- Manages vertex/index buffers for edge geometry
- Loads edge data into buffers based on terrain blend tiles
- Renders edges with alpha testing and texture blending
- Handles dynamic allocation/freeing of buffers

## Key Types
- `W3DCustomEdging` (Class): Main class managing custom edge rendering
- `detailAlphaTestShader` (ShaderClass): Shader for alpha-tested edge rendering
- `detailShader` (ShaderClass): Shader for non-alpha edge rendering
- `detailOpaqueShader` (ShaderClass): Shader for opaque edge rendering

## Key Functions
### `loadEdgingsInVertexAndIndexBuffers`
- Purpose: Loads edge geometry into vertex/index buffers based on terrain blend tiles
- Calls: `DX8IndexBufferClass::WriteLockClass`, `DX8VertexBufferClass::WriteLockClass`, `WorldHeightMap::getUVForBlend`, `WorldHeightMap::getAlphaUVData`

### `drawEdging`
- Purpose: Renders custom edges using configured shaders and textures
- Calls: `DX8Wrapper::Set_Index_Buffer`, `DX8Wrapper::Set_Vertex_Buffer`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Draw_Triangles`

### `allocateEdgingBuffers`
- Purpose: Allocates vertex/index buffers for edge geometry
- Calls: `NEW_REF` (for DX8VertexBufferClass and DX8IndexBufferClass)

## Globals
- `detailAlphaTestShader` (ShaderClass): Alpha-tested shader for edges
- `detailShader` (ShaderClass): Non-alpha shader for edges
- `detailOpaqueShader` (ShaderClass): Opaque shader for edges

## Dependencies
- `W3DCustomEdging.h`, `assetmgr.h`, `texture.h`, `common/GlobalData.h`, `common/RandomValue.h`, `W3DDevice/GameClient/TerrainTex.h`, `W3DDevice/GameClient/HeightMap.h`, `W3DDevice/GameClient/W3DDynamicLight.h`, `WW3D2/Camera.h`, `WW3D2/DX8Wrapper.h`, `WW3D2/DX8Renderer.h`, `WW3D2/Mesh.h`, `WW3D2/MeshMdl.h`
- `DX8VertexBufferClass`, `DX8IndexBufferClass`, `ShaderClass`, `WorldHeightMap`, `TextureClass`
