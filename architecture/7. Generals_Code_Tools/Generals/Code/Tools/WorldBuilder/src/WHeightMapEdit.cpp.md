# Generals/Code/Tools/WorldBuilder/src/WHeightMapEdit.cpp

## Purpose
Handles height map editing functionality in the WorldBuilder tool, including terrain texture management and cliff generation.

## Responsibilities
- Manages terrain textures and texture classes
- Handles height map data and cell processing
- Generates and adjusts cliff information for terrain edges
- Provides boundary management for map areas

## Key Types
- `WorldHeightMapEdit` (Class): Main class for height map editing
- `TGlobalTextureClass` (Struct): Stores global texture class information
- `TCliffInfo` (Struct): Contains cliff vertex and texture coordinate data

## Key Functions
### `loadBitmap`
- Purpose: Loads a TGA bitmap into a set of tiles
- Calls: `countTiles`, `readTiles`

### `updateFlatCellForAdjacentCliffs`
- Purpose: Updates cliff information for a cell based on adjacent cliffs
- Calls: `adjustForTiling`, `addCliffInfo`

### `addCliffInfo`
- Purpose: Adds cliff information to the height map
- Calls: None

### `findBoundaryNear`
- Purpose: Finds the nearest boundary to a given point
- Calls: None

## Globals
- `m_numGlobalTextureClasses` (Int): Tracks number of global texture classes
- `m_globalTextureClasses` (TGlobalTextureClass[]): Array of global texture classes
- `HEIGHT_SCALE` (Int): Height scaling factor
- `STRETCH_LIMIT` (Int): Texture stretching limit
- `TEX_PER_CELL` (Int): Texture units per cell
- `MIN_U_SPAN` (Int): Minimum U texture coordinate span
- `debugToggle` (Bool): Debug toggle flag

## Dependencies
- `StdAfx.h`, `resource.h`, `Common/STLTypedefs.h`
- `WHeightMapEdit.h`, `W3DDevice/GameClient/TileData.h`
- `TerrainModal.h`, `Common/Debug.h`
- `Common/GlobalData.h`, `Common/MapReaderWriterInfo.h`
- `Common/FileSystem.h`, `Common/TerrainTypes.h`
- `GameLogic/PolygonTrigger.h`, `GameLogic/SidesList.h`
- `rendobj.h`, `W3DDevice/GameClient/W3DShadow.h`
- `W3DDevice/GameClient/HeightMap.h`
- `Common/WellKnownKeys.h`, `mapobjectprops.h`
- `LayersList.h`, `common/DataChunk.h`
