# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/WorldHeightMap.h

## Purpose
Defines the `WorldHeightMap` class, which encapsulates height map data and terrain texture management for the game world.

## Responsibilities
- Manages height map data and terrain textures
- Handles UV mapping for terrain rendering
- Provides access to height, texture, and cliff state information
- Supports seismic effects (e.g., terrain deformation)
- Loads and parses height map data from files

## Key Types
- `WorldHeightMap` (Class): Main class for height map and terrain texture management
- `TXTextureClass` (Struct): Texture class information (global texture class, tile count, etc.)
- `TCliffInfo` (Struct): Cliff texture UV and mapping data
- `TVDirection` (Enum): Direction enum (POS_X, POS_Y, NEG_X, NEG_Y)

## Key Functions
### `getUVData`
- Purpose: Retrieves UV mapping data for a cell to map into the terrain texture.
- Calls: `getUVForNdx`, `getUVForTileIndex`

### `getAlphaUVData`
- Purpose: Retrieves UV mapping data for a cell to map into the alpha terrain texture.
- Calls: None directly visible

### `setFlipState`
- Purpose: Sets the flip state of a cell.
- Calls: None directly visible

### `getSeismicZVelocity`
- Purpose: Gets the seismic Z velocity (terrain deformation speed) at a given cell.
- Calls: None directly visible

## Globals
- `m_alphaTiles` (TileData*): Static array of alpha tiles for terrain rendering.

## Dependencies
- `Lib/BaseType.h`, `WWLib/RefCount.h`, `WWMath/Vector3.h`
- `W3DDevice/GameClient/TileData.h`
- `Common/STLTypedefs.h` (for `std::vector<ICoord2D>`)
- `MapObject.h` (for `WorldHeightMapInterfaceClass`)
- External classes: `TextureClass`, `ChunkInputStream`, `InputStream`, `OutputStream`, `DataChunkInput`, `AlphaEdgeTextureClass`
