# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/BaseHeightMap.cpp

## Purpose
Manages terrain rendering, including heightmaps, trees, and shorelines in the SAGE engine.

## Responsibilities
- Handles terrain resource management (loading/releasing)
- Renders terrain, trees, and shorelines
- Manages terrain LOD (Level of Detail) adjustments
- Controls scorch marks and water effects
- Maintains global terrain render object singleton

## Key Types
- **BaseHeightMapRenderObjClass** (Class): Base terrain rendering object
- **shoreLineTileInfo** (Struct): Stores shoreline tile vertex/UV data
- **shoreLineTileSortInfo** (Struct): Tracks sorted shoreline tile ranges

## Key Functions
### DoTrees
- Purpose: Renders transparent trees after main flush
- Calls: TheTerrainRenderObject->renderTrees

### oversizeTheTerrain
- Purpose: Adjusts terrain size by specified amount
- Calls: TheTerrainRenderObject->oversizeTerrain

### renderShoreLinesSorted
- Purpose: Renders shoreline tiles with proper sorting
- Calls: DX8Wrapper rendering functions, VertexMaterialClass methods

### renderTrees
- Purpose: Draws tree objects with proper lighting
- Calls: m_treeBuffer->drawTrees, DX8Wrapper transform/material setup

## Globals
- **TheFlatHeightMap** (FlatHeightMapRenderObjClass*): Flat terrain render object
- **TheHeightMap** (HeightMapRenderObjClass*): Detailed terrain render object
- **detailOpaqueShader** (ShaderClass): Shader for detail blending
- **TheTerrainRenderObject** (BaseHeightMapRenderObjClass*): Current terrain render object

## Dependencies
- Direct3D 8 (DX8Wrapper)
- W3D engine components (Scene, Camera)
- Terrain-specific classes (WorldHeightMap, W3DTreeBuffer)
- Shader/Texture management systems
- Global data access (TheGlobalData)
