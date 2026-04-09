# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DTerrainVisual.cpp

## Purpose
Handles W3D-specific terrain rendering, including terrain, water, shadows, and tracks.

## Responsibilities
- Manages terrain render objects and height maps
- Controls water rendering and grid effects
- Handles terrain tracks and shadows
- Processes map lights and scorch marks
- Manages terrain bibs (buildable areas)

## Key Types
- **W3DTerrainVisual (Class)**: Main terrain visual manager
- **HeightMapRenderObjClass (RefPtr)**: Terrain render object
- **WaterRenderObjClass (RefPtr)**: Water render object
- **WorldHeightMap (RefPtr)**: Terrain height map data

## Key Functions
### `init()`
- Purpose: Initializes W3D terrain systems
- Calls: `TerrainVisual::init()`, `NEW_REF`, `NEW`, `initHeightData()`

### `load()`
- Purpose: Loads terrain from file and sets up render objects
- Calls: `TerrainVisual::load()`, `NEW WorldHeightMap`, `initHeightData()`, `addScorch()`

### `intersectTerrain()`
- Purpose: Tests ray intersection with terrain
- Calls: `Cast_Ray()`

### `setWaterGridHeightClamps()`
- Purpose: Sets water grid height limits
- Calls: `setGridHeightClamps()`

### `xfer()`
- Purpose: Serializes terrain state
- Calls: `TerrainVisual::xfer()`, `xferSnapshot()`, `staticLightingChanged()`

## Globals
- **TheTerrainRenderObject (HeightMapRenderObjClass*)**: Global terrain render object
- **TheWaterRenderObj (WaterRenderObjClass*)**: Global water render object
- **TheTerrainTracksRenderObjClassSystem (TerrainTracksRenderObjClassSystem*)**: Global tracks system
- **TheW3DShadowManager (W3DShadowManager*)**: Global shadow manager

## Dependencies
- `W3DScene.h`, `W3DWater.h`, `W3DDisplay.h`, `W3DTerrainTracks.h`
- `WW3D2/RendObj.h`, `WW3D2/assetmgr.h`
- `Common/GameState.h`, `Common/GlobalData.h`
