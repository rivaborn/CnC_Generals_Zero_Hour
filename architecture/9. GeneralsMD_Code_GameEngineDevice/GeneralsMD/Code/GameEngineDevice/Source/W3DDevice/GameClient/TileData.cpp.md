# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/TileData.cpp

## Purpose
Handles texture tile data management, including mipmap generation for terrain rendering.

## Responsibilities
- Manages RGB tile data at multiple mipmap levels
- Provides access to tile data for specific resolutions
- Generates mipmaps from higher-resolution data
- Supports terrain texture rendering in the game engine

## Key Types
- **TileData (Class)**: Manages texture tile data and mipmap generation

## Key Functions
### `hasRGBDataForWidth(Int width)`
- Purpose: Checks if RGB data exists for a given width
- Calls: None

### `getRGBDataForWidth(Int width)`
- Purpose: Retrieves RGB data for a specific width
- Calls: None

### `updateMips(void)`
- Purpose: Updates all mipmap levels from the base tile data
- Calls: `doMip()`

### `doMip(UnsignedByte *pHiRes, Int hiRow, UnsignedByte *pLoRes)`
- Purpose: Generates a mipmap level from higher-resolution data
- Calls: None

## Globals
- **TILE_PIXEL_EXTENT_MIP1-MIP6 (Int)**: Constants defining mipmap resolutions (32, 16, 8, 4, 2, 1)

## Dependencies
- `TileData.h` (header for this class)
- `WorldHeightMap.h` (included but not used in this file)
- `UnsignedByte` (likely a typedef from another module)
