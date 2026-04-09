# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DRoadBuffer.cpp

## Purpose
Manages rendering of roads in the game world, including loading, updating, and drawing road segments with textures and lighting.

## Responsibilities
- Loads and manages road textures and geometry
- Handles road segment generation and culling
- Updates road lighting based on terrain
- Renders roads with appropriate shaders and textures

## Key Types
- **RoadType (Class)**: Manages road texture and geometry buffers
- **RoadSegment (Class)**: Represents individual road segments with vertices and indices
- **W3DRoadBuffer (Class)**: Main road buffer class handling road rendering
- **ShaderClass (Static)**: Predefined shaders for road rendering (detailAlphaShader, detailShader)

## Key Functions
### xpSign
- Purpose: Calculates sign of cross product to determine vector orientation
- Calls: None

### W3DRoadBuffer::loadTee
- Purpose: Loads tee-shaped road intersections into vertex buffer
- Calls: loadFloatSection

### W3DRoadBuffer::loadRoads
- Purpose: Loads all roads from map objects into buffers
- Calls: clearAllRoads, addMapObjects, updateCountsAndFlags, insertTeeIntersections, insertCurveSegments, insertCrossTypeJoins, preloadRoadsInVertexAndIndexBuffers

### W3DRoadBuffer::updateLighting
- Purpose: Updates road vertex lighting based on terrain
- Calls: RoadSegment::updateSegLighting

### W3DRoadBuffer::drawRoads
- Purpose: Renders all roads with appropriate shaders and textures
- Calls: visibilityChanged, loadRoadsInVertexAndIndexBuffers, W3DShaderManager::setShader, DX8Wrapper::Draw_Triangles

## Globals
- **TEE_WIDTH_ADJUSTMENT (Real)**: Width adjustment factor for road tees
- **detailAlphaShader (ShaderClass)**: Shader for alpha-blended road details
- **detailShader (ShaderClass)**: Shader for road mirror effects
- **CORNER_RADIUS (Real)**: Standard road corner radius
- **TIGHT_CORNER_RADIUS (Real)**: Tight road corner radius
- **s_dynamic (Bool)**: Flag for dynamic vertex/index buffers
- **warnSegments (Not inferable)**: Debug warning counter

## Dependencies
- W3DRoadBuffer.h, texture.h, assetmgr.h, common/GlobalData.h
- TerrainRoads.h, TerrainTex.h, HeightMap.h, W3DAssetManager.h
- W3DDynamicLight.h, WorldHeightMap.h, W3DShaderManager.h
- WW3D2/Camera.h, WW3D2/DX8Wrapper.h, WW3D2/DX8Renderer.h
- WW3D2/Mesh.h, WW3D2/MeshMdl.h
