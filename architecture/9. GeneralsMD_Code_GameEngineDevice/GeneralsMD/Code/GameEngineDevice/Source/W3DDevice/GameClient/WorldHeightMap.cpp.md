# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/WorldHeightMap.cpp

## Purpose
Manages terrain height maps, textures, and map objects for the game world.

## Responsibilities
- Handles height map data and terrain textures
- Manages map objects (buildings, waypoints, etc.)
- Provides terrain querying (height, texture, color)
- Supports terrain blending and cliff detection

## Key Types
- **GDIFileStream (Class)**: Wrapper for file I/O operations
- **TTargaHeader (Class)**: Structure for TGA file headers
- **MapObject (Class)**: Represents game objects in the world
- **WorldHeightMap (Class)**: Main terrain management class

## Key Functions
### `validateName`
- Purpose: Validates object names
- Calls: None

### `MapObject::duplicate`
- Purpose: Creates a copy of a map object
- Calls: `newInstance`, `getColor`, `getProperties`

### `WorldHeightMap::getTerrainTexture`
- Purpose: Generates terrain texture from height map
- Calls: `AlphaTerrainTextureClass`, `AlphaEdgeTextureClass`

### `WorldHeightMap::getTerrainColorAt`
- Purpose: Gets color at specific world coordinates
- Calls: `getSourceTile`, `getRGBDataForWidth`

### `WorldHeightMap::getRawTileData`
- Purpose: Retrieves raw tile data for rendering
- Calls: `hasRGBDataForWidth`, `getRGBDataForWidth`

## Globals
- **s_buffer (UnsignedByte[])**: Temporary buffer for tile data
- **s_blendBuffer (UnsignedByte[])**: Temporary buffer for blended tile data

## Dependencies
- `windows.h`, `stdlib.h`, `string.h`
- Common game systems: `DataChunk`, `FileSystem`, `GlobalData`
- Game logic: `PolygonTrigger`, `SidesList`
- W3D device: `WorldHeightMap.h`, `TileData.h`, `HeightMap.h`
- External: `File`, `InputStream`
