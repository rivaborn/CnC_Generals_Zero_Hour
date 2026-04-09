# Generals/Code/Tools/WorldBuilder/include/WHeightMapEdit.h

## Purpose
Header for `WorldHeightMapEdit` class, providing terrain editing functionality in WorldBuilder tool.

## Responsibilities
- Manage terrain textures, tiles, and blending
- Handle heightmap modifications and cliff adjustments
- Support map object management and boundary editing
- Provide texture optimization and validation tools

## Key Types
- **WorldHeightMapEdit (Class)**: Main terrain editing class extending `WorldHeightMap`
- **TGlobalTextureClass (Struct)**: Stores texture class data (tiles, paths, UI names)
- **CProcessNode (Class)**: Helper for texture processing nodes
- **DataChunkOutput (Class)**: External chunk output interface
- **TerrainType (Class)**: External terrain type definition

## Key Functions
### `loadBaseImages`
- Purpose: Loads default terrain textures
- Calls: `loadDirectoryOfImages`, `loadImagesFromTerrainType`

### `blendTile`
- Purpose: Blends tiles at specified coordinates
- Calls: `blendSpecificTiles`, `findOrCreateBlendTile`

### `optimizeTiles`
- Purpose: Optimizes tile memory allocation
- Calls: None visible

### `remapTextures`
- Purpose: Remaps textures to new allocations
- Calls: None visible

## Globals
- **m_numGlobalTextureClasses (int)**: Tracks number of texture classes
- **m_globalTextureClasses (TGlobalTextureClass[])**: Stores all texture class data
- **m_warnTooManyTex (Bool)**: Flag for texture warning
- **m_warnTooManyBlend (Bool)**: Flag for blend warning

## Dependencies
- `W3DDevice/GameClient/WorldHeightMap.h`
- `DataChunkOutput` (external)
- `TerrainType` (external)
- `MapObject` (external)
- `TBlendTileInfo
