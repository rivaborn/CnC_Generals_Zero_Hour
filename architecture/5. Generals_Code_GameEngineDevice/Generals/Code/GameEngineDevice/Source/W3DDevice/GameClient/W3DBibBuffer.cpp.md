# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DBibBuffer.cpp

## Purpose
Manages and renders "bibs" (2D textured quads) in the game world, such as selection highlights or markers.

## Responsibilities
- Loads and manages vertex/index buffers for bib rendering
- Handles bib creation, removal, and highlighting
- Renders bibs with proper texturing and alpha blending
- Manages texture resources for normal and highlighted bibs

## Key Types
- `W3DBibBuffer` (Class): Main class managing bib rendering
- `BibStruct` (Struct): Stores bib data (corners, highlight state, etc.)
- `detailAlphaShader` (ShaderClass): Shader for alpha-blended textured rendering

## Key Functions
### `loadBibsInVertexAndIndexBuffers`
- Purpose: Packs bib data into vertex/index buffers for rendering
- Calls: `DX8IndexBufferClass::WriteLockClass`, `DX8VertexBufferClass::WriteLockClass`

### `renderBibs`
- Purpose: Renders all active bibs with proper texturing and culling
- Calls: `loadBibsInVertexAndIndexBuffers`, `DX8Wrapper::Set_Index_Buffer`, `DX8Wrapper::Set_Vertex_Buffer`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Draw_Triangles`

### `addBib`/`addBibDrawable`
- Purpose: Adds a new bib to the buffer
- Calls: None (direct member access)

### `removeBib`/`removeBibDrawable`
- Purpose: Marks a bib for removal
- Calls: None (direct member access)

## Globals
- `detailAlphaShader` (ShaderClass): Static shader for alpha-blended rendering

## Dependencies
- `W3DBibBuffer.h` (header)
- `texture.h`, `assetmgr.h`, `common/GlobalData.h`, `common/RandomValue.h`
- `W3DDevice/GameClient/TerrainTex.h`, `W3DDevice/GameClient/HeightMap.h`
- `W3DDevice/GameClient/W3DDynamicLight.h`
- `WW3D2/Camera.h`, `WW3D2/DX8Wrapper.h`, `WW3D2/DX8Renderer.h`
- `WW3D2/Mesh.h`, `WW3D2/MeshMdl.h`
