# GeneralsMD/Code/GameEngine/Source/GameClient/MapUtil.cpp

## Purpose
Handles map loading, parsing, validation, and utility functions for the game client.

## Responsibilities
- Load and parse map files (heightmaps, objects, waypoints)
- Manage map metadata and caching
- Validate and select default maps
- Generate map previews
- Calculate map extents and boundaries

## Key Types
- **MapCache (Class)**: Manages cached map metadata
- **MapMetaData (Struct)**: Stores map properties (size, multiplayer flag, etc.)
- **WaypointMap (Class)**: Tracks waypoint positions
- **Region3D (Struct)**: Defines 3D spatial extents

## Key Functions
### `loadMap`
- Purpose: Loads and parses a map file
- Calls: `CachedFileInputStream::open`, `DataChunkInput::parse`, `ParseSizeOnlyInChunk`, `ParseWorldDictDataChunk`, `ParseObjectsDataChunk`

### `isValidMap`
- Purpose: Checks if a map exists and is valid for the given mode
- Calls: `MapCache::updateCache`, `MapCache::find`

### `getMapPreviewImage`
- Purpose: Retrieves or generates a preview image for a map
- Calls: `TheMappedImageCollection::findImageByName`, `copyFromBigToDir`

### `findDrawPositions`
- Purpose: Calculates screen positions for drawing a map preview
- Calls: None

## Globals
- **mapExtension (char*)**: Stores the ".map" file extension
- **m_width/m_height (Int)**: Map dimensions
- **m_boundaries (vector<ICoord2D>)**: Map boundary coordinates
- **m_data (UnsignedByte*)**: Heightmap data
- **TheMapCache (MapCache*)**: Global map cache instance

## Dependencies
- Common: `CRC`, `FileSystem`, `DataChunk`, `MapReaderWriterInfo`
- GameClient: `GameText`, `Image`, `GadgetListBox`
- GameLogic: `ThingFactory`, `ThingTemplate`
- GameNetwork: `GameInfo`
