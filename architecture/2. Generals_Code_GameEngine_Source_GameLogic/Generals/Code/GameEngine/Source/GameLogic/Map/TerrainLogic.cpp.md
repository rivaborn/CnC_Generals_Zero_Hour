# Generals/Code/GameEngine/Source/GameLogic/Map/TerrainLogic.cpp

## Purpose
Handles terrain logic, including bridge creation, terrain flattening, and water updates.

## Responsibilities
- Manage bridges and their towers.
- Flatten terrain beneath structures.
- Update water levels dynamically.
- Handle map boundary adjustments.

## Key Types
- **Waypoint (struct)**: Represents waypoints with links and labels.
- **BridgeInfo (struct)**: Stores information about a bridge.
- **Bridge (class)**: Manages bridge objects and their towers.
- **TerrainLogic (class)**: Main class for terrain logic operations.

## Key Functions
### flattenTerrain
- Purpose: Flattens the terrain beneath structures.
- Calls:
  - `getGeometryInfo()`
  - `getPosition()`
  - `setRawMapHeight()`

### crc
- Purpose: Handles CRC operations (empty implementation).

### xfer
- Purpose: Handles serialization and deserialization of terrain logic data.
- Calls:
  - `xferVersion()`
  - `xferInt()`
  - `xferReal()`

### loadPostProcess
- Purpose: Post-processes loaded data to ensure consistency.
- Calls:
  - `getFirstBridge()`
  - `findObjectByID()`
  - `deleteBridge()`

## Globals
- **TheTerrainLogic (TerrainLogic \*)**: Global instance of TerrainLogic.

## Dependencies
- Key includes:
  - "Common/DataChunk.h"
  - "Common/GameState.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/TerrainLogic.h"
  - "WWMath/plane.h"
  - "WWMath/tri.h"

- External symbols used:
  - `TheThingFactory`
  - `TheTerrainRoads`
  - `ThePartitionManager`
  - `TheGhostObjectManager`
  - `TheGameLogic`
  - `TheRadar`
  - `TheTacticalView`
