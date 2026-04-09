# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/HeightMap.cpp

## Purpose
Handles terrain rendering, including lighting, texturing, and special effects like shorelines and extra texture blends.

## Responsibilities
- Manages terrain vertex/index buffers and shaders
- Computes lighting for terrain vertices (static and dynamic)
- Renders special terrain effects (shorelines, extra blends)
- Handles tree rendering for transparent objects
- Provides utility functions for terrain manipulation

## Key Types
- `HeightMapRenderObjClass`: Main terrain rendering object
- `VERTEX_FORMAT`: Vertex data structure for terrain
- `ShaderClass`: Shader configuration for rendering
- `shoreLineTileInfo`: Stores shoreline tile data

## Key Functions
### `DoTrees`
- Purpose: Renders trees after transparent objects are flushed
- Calls: `TheTerrainRenderObject->renderTrees`

### `oversizeTheTerrain`
- Purpose: Adjusts terrain size by specified amount
- Calls: `TheTerrainRenderObject->oversizeTerrain`

### `doTheLight`
- Purpose: Computes static lighting for terrain vertices
- Calls: `Vector3::Dot_Product`, `WWMath::Clamp`

### `doTheDynamicLight`
- Purpose: Computes dynamic lighting for terrain vertices
- Calls: `Vector3::Dot_Product`, `WWMath::Clamp`, `WWMath::Float_To_Int_Chop`

### `renderShoreLines`
- Purpose: Renders smooth transitions between land and water
- Calls: `DX8Wrapper::Set_Shader`, `DX8Wrapper::Draw_Triangles`

### `renderExtraBlendTiles`
- Purpose: Renders terrain tiles with 3+ texture blends
- Calls: `DX8Wrapper::Set_Shader`, `DX8Wrapper::Draw_Triangles`

## Globals
- `detailOpaqueShader` (ShaderClass): Shader for detail blending
- `TheTerrainRenderObject` (HeightMapRenderObjClass*): Singleton terrain renderer
- `visMinX/Y/visMaxX/Y` (Int): Visibility bounds for terrain rendering

## Dependencies
- Direct3D 8 (DX8Wrapper)
- W3D engine components (Scene, Camera, Light)
- Game-specific systems (TerrainLogic, Water, Shroud)
- Math utilities (Vector3, WWMath)
- Asset management (Texture, AssetMgr)
