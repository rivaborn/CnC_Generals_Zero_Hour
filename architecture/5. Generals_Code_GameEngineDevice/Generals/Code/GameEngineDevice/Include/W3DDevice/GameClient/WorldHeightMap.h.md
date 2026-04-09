# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/WorldHeightMap.h

## Purpose
Defines the `WorldHeightMap` class, which encapsulates height map data and terrain texture management for the game world.

## Responsibilities
- Manages height map data and terrain textures
- Handles UV mapping for terrain rendering
- Processes cliff and blend tile information
- Provides access to terrain height and texture data
- Supports serialization/deserialization of map data

## Key Types
- `WorldHeightMap` (Class): Main class for height map and terrain texture management
- `TXTextureClass` (Struct): Stores texture class information (global texture class, tile count, etc.)
- `TCliffInfo` (Struct): Contains UV coordinates and flip/mutant flags for cliff textures
- `TVDirection` (Enum): Direction enum for texture mapping (POS_X, POS_Y, NEG_X, NEG_Y)

## Key Functions
### `getUVData`
- Purpose: Retrieves UV mapping data for a cell in the terrain texture
- Calls: `getUVForNdx`, `getUVForTileIndex`

### `getAlphaUVData`
- Purpose: Retrieves UV mapping data for alpha terrain textures
- Calls: Not inferable

### `ParseHeightMapData`
- Purpose: Parses height map data from a chunk input stream
- Calls: Not inferable

### `setDrawOrg`
- Purpose: Sets the drawing origin for the height map
- Calls: Not inferable

## Globals
- `NUM_SOURCE_TILES` (Int): Maximum number of source tiles (1024)
- `NUM_BLEND_TILES` (Int): Maximum number of blend tiles (16192)
- `NUM_CLIFF_INFO` (Int): Maximum number of cliff info entries (32384)
- `FLAG_VAL` (Int): Flag value for texture mapping (0x7ADA0000)

## Dependencies
- `Lib/BaseType.h`, `WWLib/RefCount.h`, `WWMath/Vector3.h`
- `W3DDevice/GameClient/TileData.h`
- `Common/STLTypedefs.h` (for `std::vector`)
- `TerrainTextureClass`, `AlphaTerrainTextureClass`, `AlphaEdgeTextureClass` (forward declarations)
