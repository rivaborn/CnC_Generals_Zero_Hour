# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DBibBuffer.cpp

## Purpose
Manages and renders "bibs" (decal-like textures) on terrain in the game world.

## Responsibilities
- Loads and manages vertex/index buffers for bib rendering
- Handles bib addition/removal by object or drawable ID
- Applies textures and shaders for transparent rendering
- Supports highlighting of bibs

## Key Types
- `W3DBibBuffer` (Class): Main class managing bib rendering
- `BibStruct` (Struct): Stores bib corner positions, highlight state, and IDs
- `detailAlphaShader` (ShaderClass): Predefined shader for alpha-blended rendering

## Key Functions
### `loadBibsInVertexAndIndexBuffers`
- Purpose: Packs bib geometry into GPU buffers
- Calls: `DX8IndexBufferClass::WriteLockClass`, `DX8VertexBufferClass::WriteLockClass`

### `renderBibs`
- Purpose: Renders all active bibs with proper texturing
- Calls: `loadBibsInVertexAndIndexBuffers`, `DX8Wrapper::Set_*`, `DX8Wrapper::Draw_Triangles`

### `addBib`/`addBibDrawable`
- Purpose: Adds new bibs to the buffer
- Calls: None (direct member access)

### `removeBib`/`removeBibDrawable`
- Purpose: Marks bibs for removal
- Calls: None (direct member access)

## Globals
- `detailAlphaShader` (ShaderClass): Static shader for alpha-blended rendering

## Dependencies
- `W3DBibBuffer.h`, `texture.h`, `assetmgr.h`, `WW3D2/` headers
- `DX8Wrapper`, `DX8Renderer`, `DX8VertexBufferClass`, `DX8IndexBufferClass`
- `TextureClass`, `ShaderClass`, `Vector3`, `GlobalData`
