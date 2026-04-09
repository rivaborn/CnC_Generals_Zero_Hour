# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DTerrainVisual.h

## Purpose
Header defining the W3DTerrainVisual class, which handles visual terrain rendering and water effects in the SAGE engine.

## Responsibilities
- Manages terrain rendering and water effects
- Provides terrain intersection and height queries
- Handles dynamic water grid adjustments
- Manages faction-specific terrain decorations (bibs)
- Supports seismic simulations (conditional)

## Key Types
- **W3DTerrainVisual (Class)**: Main terrain visual manager
- **Matrix3D (Class)**: 3D transformation matrix
- **WaterHandle (Class)**: Handle for water grid operations
- **BaseHeightMapRenderObjClass (Class)**: Base terrain render object
- **WorldHeightMap (Class)**: Height map data structure

## Key Functions
### W3DTerrainVisual::init
- Purpose: Initialize terrain visual system
- Calls: Not inferable

### W3DTerrainVisual::load
- Purpose: Load terrain from file
- Calls: Not inferable

### W3DTerrainVisual::intersectTerrain
- Purpose: Ray-terrain intersection test
- Calls: Not inferable

### W3DTerrainVisual::enableWaterGrid
- Purpose: Enable/disable water grid rendering
- Calls: Not inferable

### W3DTerrainVisual::setWaterTransform
- Purpose: Set water plane transformation
- Calls: Not inferable

### W3DTerrainVisual::addFactionBib
- Purpose: Add faction-specific terrain decoration
- Calls: Not inferable

### W3DTerrainVisual::removeTreesAndPropsForConstruction
- Purpose: Clear terrain objects for construction
- Calls: Not inferable

## Globals
- **m_terrainRenderObject (BaseHeightMapRenderObjClass**)**: Terrain render object
- **m_waterRenderObject (WaterRenderObjClass**)**: Water render object
- **m_logicHeightMap (WorldHeightMap**)**: Height map for rendering
- **m_isWaterGridRenderingEnabled (Bool)**: Water grid state flag

## Dependencies
- **TerrainVisual.h**: Base terrain visual interface
- **W3DWater.h**: Water rendering definitions
- **Matrix3D, WaterHandle, BaseHeightMapRenderObjClass, WorldHeightMap**: Forward-declared classes
