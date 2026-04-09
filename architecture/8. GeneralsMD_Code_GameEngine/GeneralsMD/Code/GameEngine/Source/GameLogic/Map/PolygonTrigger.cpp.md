# GeneralsMD/Code/GameEngine/Source/GameLogic/Map/PolygonTrigger.cpp

## Purpose
Manages polygon trigger areas in the game map, handling serialization, point manipulation, and spatial queries.

## Responsibilities
- Encapsulates polygon trigger logic for map areas
- Manages trigger point lists and bounds
- Handles serialization/deserialization of triggers
- Provides point-in-polygon testing
- Maintains water area and river trigger functionality

## Key Types
- **PolygonTrigger (Class)**: Main class representing a polygon trigger area
- **WaterHandle (Struct)**: Handles water area functionality for triggers
- **ICoord3D (Struct)**: 3D coordinate point used for polygon vertices

## Key Functions
### `ParsePolygonTriggersDataChunk`
- Purpose: Reads polygon triggers from a data chunk
- Calls: `deleteTriggers`, `newInstance`, `addPolygonTrigger`

### `WritePolygonTriggersDataChunk`
- Purpose: Writes polygon triggers to a data chunk
- Calls: `openDataChunk`, `writeInt`, `writeAsciiString`, `writeByte`

### `pointInTrigger`
- Purpose: Tests if a point lies inside the polygon trigger
- Calls: `updateBounds`

### `updateBounds`
- Purpose: Updates the bounding box and radius of the trigger
- Calls: `None`

## Globals
- **ThePolygonTriggerListPtr (PolygonTrigger*)**: Head of the linked list of triggers
- **s_currentID (Int)**: Counter for assigning unique trigger IDs

## Dependencies
- Common/DataChunk.h
- Common/MapObject.h
- Common/MapReaderWriterInfo.h
- Common/Xfer.h
- GameLogic/PolygonTrigger.h
- GameLogic/TerrainLogic.h
