# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DTerrainVisual.h

## Purpose
Header for W3DTerrainVisual class, handling visual aspects of terrain rendering in the SAGE engine.

## Responsibilities
- Manages terrain rendering (heightmaps, textures, skybox)
- Controls water grid rendering and physics
- Handles terrain intersection and color queries
- Manages faction-specific terrain decorations (bibs)
- Provides terrain modification capabilities

## Key Types
- **W3DTerrainVisual (Class)**: Main terrain visual manager
- **Matrix3D (Class)**: 3D transformation matrix
- **WaterHandle (Class)**: Handle for water grid operations
- **HeightMapRenderObjClass (Class)**: Terrain render object
- **WorldHeightMap (Class)**: Heightmap data structure

## Key Functions
### `init()`
- Purpose: Initialize terrain visual system
- Calls: Not inferable

### `load()`
- Purpose: Load terrain from file
- Calls: Not inferable

### `intersectTerrain()`
- Purpose: Ray-terrain intersection test
- Calls: Not inferable

### `enableWaterGrid()`
- Purpose: Enable/disable water grid rendering
- Calls: Not inferable

### `setWaterTransform()`
- Purpose: Set water grid position/orientation
- Calls: Not inferable

### `addFactionBib()`
- Purpose: Add faction-specific terrain decoration
- Calls: Not inferable

### `setRawMapHeight()`
- Purpose: Modify terrain height at specific grid position
- Calls: Not inferable

## Globals
- **m_terrainRenderObject (HeightMapRenderObjClass*)**: Terrain render object
- **m_waterRenderObject (WaterRenderObjClass*)**: Water render object
- **m_terrain
