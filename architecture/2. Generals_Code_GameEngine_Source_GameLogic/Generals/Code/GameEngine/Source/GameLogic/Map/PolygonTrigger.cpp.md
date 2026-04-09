# Generals/Code/GameEngine/Source/GameLogic/Map/PolygonTrigger.cpp

## Purpose
This file defines the `PolygonTrigger` class, which encapsulates polygon trigger areas used in the game's map logic.

## Responsibilities
- Manage polygon triggers for defining areas on the map.
- Handle parsing and writing of polygon trigger data chunks.
- Provide methods to add, remove, and check points within a polygon.
- Determine if a point is inside a polygon trigger area.

## Key Types
- `PolygonTrigger` (Class): Manages polygon trigger areas with points and properties like water or river status.

## Key Functions
### PolygonTrigger::reallocate
- Purpose: Increases the size of the points list.
- Calls: None

### PolygonTrigger::getPolygonTriggerByID
- Purpose: Finds a polygon trigger by its ID.
- Calls: `getNext`

### PolygonTrigger::ParsePolygonTriggersDataChunk
- Purpose: Reads polygon triggers from a data chunk.
- Calls: `readInt`, `readAsciiString`, `readByte`, `newInstance`, `setTriggerName`, `setWaterArea`, `setRiver`, `addPoint`, `atEndOfChunk`

### PolygonTrigger::WritePolygonTriggersDataChunk
- Purpose: Writes polygon triggers to a data chunk.
- Calls: `openDataChunk`, `writeInt`, `writeAsciiString`, `writeByte`, `closeDataChunk`

### PolygonTrigger::updateBounds
- Purpose: Updates the bounding box and radius of the polygon.
- Calls: None

### PolygonTrigger::addPolygonTrigger
- Purpose: Adds a trigger to the list of triggers.
- Calls: `getNext`

### PolygonTrigger::removePolygonTrigger
- Purpose: Removes a trigger from the list of triggers.
- Calls: `getNext`

### PolygonTrigger::deleteTriggers
- Purpose: Deletes all polygon triggers.
- Calls: `deleteInstance`

### PolygonTrigger::addPoint
- Purpose: Adds a point to the polygon.
- Calls: `reallocate`

### PolygonTrigger::setPoint
- Purpose: Sets a point at a specific index.
- Calls: `addPoint`, `updateBounds`

### PolygonTrigger::insertPoint
- Purpose: Inserts a point at a specific index.
- Calls: `reallocate`, `updateBounds`

### PolygonTrigger::deletePoint
- Purpose: Deletes a point at a specific index.
- Calls: `updateBounds`

### PolygonTrigger::getCenterPoint
- Purpose: Calculates the center point of the polygon.
- Calls: `updateBounds`, `getGroundHeight`

### PolygonTrigger::getRadius
- Purpose: Returns the radius of the polygon.
- Calls: `updateBounds`

### PolygonTrigger::pointInTrigger
- Purpose: Checks if a point is inside the polygon.
- Calls: `updateBounds`

## Globals
- `ThePolygonTriggerListPtr` (Pointer): Head of the list of polygon triggers.
- `s_currentID` (Int): Current ID for new polygon triggers.

## Dependencies
- Key includes:
  - "Common/DataChunk.h"
  - "Common/MapObject.h"
  - "Common/MapReaderWriterInfo.h"
  - "Common/Xfer.h"
  - "GameLogic/PolygonTrigger.h"
  - "GameLogic/TerrainLogic.h"

- External symbols used but not defined here:
  - `DataChunkInput`
  - `DataChunkOutput`
  - `ICoord3D`
  - `Coord3D`
  - `IRegion2D`
  - `Xfer`
  - `TheGlobalData`
  - `MAP_XY_FACTOR`
  - `TheTerrainLogic`
