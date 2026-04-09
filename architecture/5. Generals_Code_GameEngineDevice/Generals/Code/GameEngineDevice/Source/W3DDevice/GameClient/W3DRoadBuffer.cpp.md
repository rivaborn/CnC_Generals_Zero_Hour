# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DRoadBuffer.cpp

## Purpose
Manages rendering of road segments in the game world, handling geometry generation, texturing, and lighting.

## Responsibilities
- Generates and renders road geometry from map data
- Manages road textures and shaders
- Handles road segment connections and intersections
- Updates lighting for road segments
- Supports wireframe and normal rendering modes

## Key Types
- `RoadType` (Class): Manages road texture and vertex/index buffers
- `RoadSegment` (Class): Represents individual road segments with vertex/index data
- `W3DRoadBuffer` (Class): Main road rendering manager
- `ShaderClass` (Struct): Defines shader configurations for road rendering

## Key Functions
### `xpSign`
- Purpose: Calculates sign of cross product to determine vector orientation
- Calls: None

### `W3DRoadBuffer::loadTee`
- Purpose: Loads tee-shaped road intersections into vertex buffer
- Calls: `loadFloatSection`

### `W3DRoadBuffer::loadAlphaJoin`
- Purpose: Loads alpha-blended road joins for smooth transitions
- Calls: None

### `W3DRoadBuffer::loadRoads`
- Purpose: Loads all roads from map objects into rendering buffers
- Calls: `clearAllRoads`, `addMapObjects`, `updateCountsAndFlags`, `insertTeeIntersections`, `insertCurveSegments`, `insertCrossTypeJoins`, `preloadRoadsInVertexAndIndexBuffers`

### `W3DRoadBuffer::drawRoads`
- Purpose: Renders all road segments with proper texturing and lighting
- Calls: `W3DShaderManager::setShader`, `DX8Wrapper::Draw_Triangles`

## Globals
- `TEE_WIDTH_ADJUSTMENT` (Real): Width adjustment factor for tee intersections
- `detailAlphaShader` (ShaderClass): Shader for alpha-blended road details
- `detailShader` (ShaderClass): Shader for road rendering
- `CORNER_RADIUS` (Real): Radius for standard road corners
- `TIGHT_CORNER_RADIUS` (Real): Radius for tight road corners
- `warnSegments` (Bool): Debug flag for segment warnings

## Dependencies
- `W3DRoadBuffer.h` (header)
- `DX8Wrapper.h`, `DX8Renderer.h` (DirectX rendering)
- `W3DShaderManager.h` (shader management)
- `TerrainRoads.h`, `WorldHeightMap.h` (terrain data)
- `WW3D2/Camera.h` (camera system)
- `Common/GlobalData.h` (game globals)
