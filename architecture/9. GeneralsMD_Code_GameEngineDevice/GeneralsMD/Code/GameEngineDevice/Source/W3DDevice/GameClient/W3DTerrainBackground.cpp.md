# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DTerrainBackground.cpp

## Purpose
Manages low-resolution terrain rendering for background terrain in the SAGE engine.

## Responsibilities
- Handles terrain vertex/index buffer management
- Implements tesselated terrain updates
- Manages terrain texture LOD (Level of Detail) switching
- Performs frustum culling for terrain rendering
- Supports terrain flipping for optimization

## Key Types
- `W3DTerrainBackground` (Class): Main terrain background manager
- `detailShader` (ShaderClass): Shader for alpha-textured terrain rendering
- `VertexFormatXYZDUV2` (Struct): Vertex format for terrain vertices

## Key Functions
### `doTesselatedUpdate`
- Purpose: Updates a partial block of terrain vertices with tesselation
- Calls: `setFlip`, `fillVBRecursive`, `m_map->getFlatTexture`

### `updateCenter`
- Purpose: Updates culling status and texture LOD based on camera position
- Calls: `camera->Cull_Box`, `m_terrainTexture->setLOD`

### `drawVisiblePolys`
- Purpose: Renders visible terrain polygons
- Calls: `DX8Wrapper::Set_Index_Buffer`, `DX8Wrapper::Set_Vertex_Buffer`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Draw_Triangles`

### `fillVBRecursive`
- Purpose: Recursively fills index buffer with terrain indices
- Calls: `advanceLeft`, `advanceRight`

## Globals
- `detailShader` (ShaderClass): Static shader for terrain rendering
- `PIXELS_PER_GRID` (Int): Default texture resolution per tile
- `STEP` (Int): Step size for terrain tesselation

## Dependencies
- `W3DTerrainBackground.h`
- `DX8VertexBufferClass`, `DX8IndexBufferClass`
- `WorldHeightMap`, `TerrainTextureClass`
- `DX8Wrapper`, `CameraClass`
- `MinMaxAABoxClass`, `Vector3`
