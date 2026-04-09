# GeneralsMD/Code/GameEngine/Include/GameLogic/PolygonTrigger.h

## Purpose
Defines the PolygonTrigger class for handling polygon-based map triggers, including area triggers for scripts and water areas.

## Responsibilities
- Manages polygon triggers for map scripting and water areas
- Handles point manipulation and polygon bounds
- Supports serialization via Snapshot interface
- Maintains linked list of triggers
- Provides water area functionality via WaterHandle

## Key Types
- **PolygonTrigger (Class)**: Main class for polygon triggers with point management and trigger logic
- **WaterHandle (Class)**: Handle for water areas, references a PolygonTrigger
- **PolygonTriggerMagicEnum (Enum)**: Not inferable (empty enum)
- **PolygonTrigger_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### `addPoint`
- Purpose: Adds a point to the polygon
- Calls: `reallocate`, `updateBounds`

### `pointInTrigger`
- Purpose: Checks if a point is inside the polygon
- Calls: None visible

### `updateBounds`
- Purpose: Updates the 2D bounding box and radius
- Calls: None visible

### `ParsePolygonTriggersDataChunk`
- Purpose: Parses polygon trigger data from a chunk
- Calls: None visible

### `WritePolygonTriggersDataChunk`
- Purpose: Writes polygon trigger data to a chunk
- Calls: None visible

## Globals
- **ThePolygonTriggerListPtr (PolygonTrigger*)**: Head of the linked list of triggers
- **s_currentID (Int)**: Counter for generating unique trigger IDs

## Dependencies
- `Common/GameMemory.h`, `Common/Snapshot.h`, `Common/STLTypedefs.h`
- `DataChunkInput`, `DataChunkOutput`, `DataChunkInfo`, `Xfer` (forward
