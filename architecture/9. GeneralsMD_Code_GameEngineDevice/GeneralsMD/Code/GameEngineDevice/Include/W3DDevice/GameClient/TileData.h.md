# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/TileData.h

## Purpose
Manages bitmap data for a single tile used in texture creation and rendering.

## Responsibilities
- Stores tile bitmap data in BGRA format
- Manages mipmap levels for the tile
- Provides access to tile data at different resolutions
- Handles texture coordinate tracking

## Key Types
- **TBlendTileInfo (struct)**: Stores blend information for tile edges (horiz/vert diagonals, inversion, custom blend class)
- **TileData (class)**: Holds tile bitmap data and mipmaps, provides access methods

## Key Functions
### doMip
- Purpose: Generates next mip level from higher resolution data
- Calls: None

### updateMips
- Purpose: Updates all mipmap levels for the tile
- Calls: doMip

### hasRGBDataForWidth
- Purpose: Checks if RGB data exists for specified width
- Calls: None

### getRGBDataForWidth
- Purpose: Returns RGB data pointer for specified width
- Calls: None

## Globals
- **INVERTED_MASK (Int)**: Bitmask for inverted state in blend info
- **FLIPPED_MASK (Int)**: Bitmask for flipped state in blend info
- **TILE_PIXEL_EXTENT (Int)**: Tile dimensions (64x64)
- **DATA_LEN_BYTES (Int)**: Total tile data size in bytes
- **TEXTURE_WIDTH (Int)**: Maximum texture width (2048)

## Dependencies
- `Lib/BaseType.h` (Int, UnsignedByte)
- `WWLib/RefCount.h` (RefCountClass)
- `Common/AsciiString.h` (ICoord2D)
