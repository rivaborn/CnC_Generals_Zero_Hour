# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/FlatHeightMap.cpp

## Purpose
Manages rendering of flat terrain heightmaps in the game engine.

## Responsibilities
- Initializes and manages terrain tiles
- Handles terrain rendering with LOD (Level of Detail) adjustments
- Updates terrain based on lighting and camera position
- Manages terrain textures and shaders
- Handles special terrain effects (shorelines, roads, scorches)

## Key Types
- `FlatHeightMapRenderObjClass` (Class): Main terrain rendering class
- `W3DTerrainBackground` (Class): Represents individual terrain tiles
- `ShaderClass` (Class): Handles shader management
- `detailOpaqueShader` (Static): Shader for detail rendering

## Key Functions
### `FlatHeightMapRenderObjClass::initHeightData`
- Purpose: Initializes terrain height data and rendering resources
- Calls: `BaseHeightMapRenderObjClass::initHeightData`, `W3DTerrainBackground::allocateTerrainBuffers`, `W3DTerrainBackground::doPartialUpdate`

### `FlatHeightMapRenderObjClass::Render`
- Purpose: Renders the terrain with appropriate shaders and textures
- Calls: `DX8Wrapper::Set_Transform`, `DX8Wrapper::Set_Material`, `W3DShaderManager::setShader`, `W3DTerrainBackground::drawVisiblePolys`, `renderShoreLines`

### `FlatHeightMapRenderObjClass::updateCenter`
- Purpose: Updates terrain rendering based on camera position
- Calls: `BaseHeightMapRenderObjClass::updateCenter`, `W3DTerrainBackground::updateCenter`

### `FlatHeightMapRenderObjClass::staticLightingChanged`
- Purpose: Recalculates lighting for all terrain tiles
- Calls: `BaseHeightMapRenderObjClass::staticLightingChanged`, `W3DTerrainBackground::doPartialUpdate`

## Globals
- `TheFlatHeightMap` (FlatHeightMapRenderObjClass*): Global instance of the terrain renderer
- `detailOpaqueShader` (ShaderClass): Static shader for detail rendering
- `CELLS_PER_TILE` (const Int): Number of cells per terrain tile (16)

## Dependencies
- Key includes: `FlatHeightMap.h`, `W3DTerrainBackground.h`, `W3DShaderManager.h`, `DX8Wrapper.h`
- External symbols: `TheGlobalData`, `TheTerrainRenderObject`, `Scene`, `DX8Wrapper` functions
