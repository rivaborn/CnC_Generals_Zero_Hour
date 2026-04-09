# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/HeightMap.cpp

## Purpose
Handles terrain rendering, including heightmap visualization, dynamic lighting, and special effects like shorelines and scorch marks.

## Responsibilities
- Manages vertex/index buffers for terrain geometry
- Applies dynamic lighting to terrain vertices
- Renders terrain with multiple texture layers and blending
- Handles special terrain effects (shorelines, extra blends, shrouds)
- Supports low-resolution mesh rendering for performance

## Key Types
- **HeightMapRenderObjClass**: Main terrain rendering class
- **VERTEX_FORMAT**: Vertex structure for terrain rendering
- **ShaderClass**: Shader configuration for terrain rendering
- **WorldHeightMap**: Heightmap data structure

## Key Functions
### doTheDynamicLight
- Purpose: Calculates diffuse lighting affected by dynamic lights
- Calls: Vector3 operations, W3DDynamicLight methods

### updateVB
- Purpose: Updates vertex buffer data for a rectangular terrain region
- Calls: DX8VertexBufferClass, WorldHeightMap methods

### renderExtraBlendTiles
- Purpose: Renders terrain tiles with 3-texture blending
- Calls: DynamicVBAccessClass, DynamicIBAccessClass, W3DShaderManager

### renderTerrainPass
- Purpose: Performs additional rendering pass for terrain (shroud effects)
- Calls: DX8Wrapper rendering functions

## Globals
- **HALF_RES_MESH** (Bool): Controls whether to use half-resolution mesh
- **TheHeightMap** (HeightMapRenderObjClass*): Global heightmap instance
- **detailOpaqueShader** (ShaderClass): Shader for detail rendering
- **visMinX/visMinY/visMaxX/visMaxY** (Int): Visibility bounds

## Dependencies
- W3DDevice/GameClient/heightmap.h
- DX8Wrapper.h, Scene.h (WW3D2)
- W3DShaderManager.h, TerrainTex.h
- GameLogic/TerrainLogic.h, AIPathfind.h
- Common/GlobalData.h, PerfTimer.h
