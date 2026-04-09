# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameLogic/W3DTerrainLogic.cpp

## Purpose
Implements W3D-specific terrain logic for the game engine, handling heightmap data, terrain boundaries, and pathfinding-related terrain queries.

## Responsibilities
- Loads and manages terrain heightmap data
- Provides terrain height and normal queries
- Handles terrain boundaries and map extents
- Supports line-of-sight and cliff detection
- Manages terrain layers (ground, walls, bridges)

## Key Types
- `W3DTerrainLogic` (Class): Main terrain logic class for W3D rendering
- `WorldHeightMap` (Class): Holds raw heightmap data samples
- `Region3D` (Struct): 3D spatial region definition
- `Coord3D` (Struct): 3D coordinate point
- `PathfindLayerEnum` (Enum): Terrain layer types (ground, wall, bridge)

## Key Functions
### `loadMap`
- Purpose: Loads terrain heightmap data from file
- Calls: `WorldHeightMap` constructor, `TerrainLogic::loadMap`, `TheGameClient->setTimeOfDay`

### `getGroundHeight`
- Purpose: Returns terrain height at given coordinates
- Calls: `TheTerrainRenderObject->getHeightMapHeight`

### `getLayerHeight`
- Purpose: Returns height considering terrain layers (ground/wall/bridge)
- Calls: `TheTerrainRenderObject->getHeightMapHeight`, `TheAI->pathfinder()->isPointOnWall`, `findBridgeLayerAt`

### `isClearLineOfSight`
- Purpose: Checks if line of sight is clear between two points
- Calls: `TheTerrainRenderObject->isClearLineOfSight`

### `getExtent`
- Purpose: Gets the 3D extent of the terrain in world coordinates
- Calls: None

## Globals
- `TheTerrainRenderObject` (External): Terrain rendering object
- `TheMapCache` (External): Map cache system
- `TheGlobalData` (External): Global game data
- `TheWritableGlobalData` (External): Writable global game data
- `TheGameClient` (External): Game client interface
- `TheAI` (External): AI system

## Dependencies
- `Common/GameMemory.h`
- `W3DDevice/GameClient/HeightMap.h`
- `W3DDevice/GameLogic/W3DTerrainLogic.h`
- `W3DDevice/GameClient/WorldHeightMap.h`
- `Common/PerfTimer.h`
- `Common/MapReaderWriterInfo.h`
- `Common/GlobalData.h`
- `Common/Xfer.h`
- `GameClient/GameClient.h`
- `GameClient/Map
