# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/TileData.h

## Purpose
Manages bitmap data for a single tile used in rendering and texture creation.

## Responsibilities
- Stores tile pixel data in BGRA format
- Manages mipmap levels for the tile
- Provides access to tile data at different resolutions
- Handles texture coordinate tracking

## Key Types
- TBlendTileInfo (struct): Stores blend information for tile edges (horiz/vert diagonals, inversion, custom blend class)
- TileData (class): Holds tile bitmap data and mipmaps, inherits from RefCountClass

## Key Functions
### doMip
- Purpose: Generates a mipmap level from higher resolution data
- Calls: None

### updateMips
- Purpose: Updates all mipmap levels for the tile
- Calls: doMip

### getRGBDataForWidth
- Purpose: Retrieves tile data at specified width (original or mipmapped)
- Calls: None

## Globals
- None

## Dependencies
- Lib/BaseType.h (Int, UnsignedByte)
- WWLib/RefCount.h (RefCountClass)
- Common/AsciiString.h (ICoord2D)
