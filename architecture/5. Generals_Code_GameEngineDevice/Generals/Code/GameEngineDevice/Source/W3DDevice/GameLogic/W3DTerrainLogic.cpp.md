# Generals/Code/GameEngineDevice/Source/W3DDevice/GameLogic/W3DTerrainLogic.cpp

## Purpose
Handles W3D-specific terrain logic for the game engine, including heightmap loading, boundary management, and terrain queries.

## Responsibilities
- Loads and manages terrain heightmap data
- Provides terrain extent and height queries
- Handles line-of-sight calculations
- Manages map boundaries and pathfinding extents
- Supports layer-based height queries (ground, walls, bridges)

## Key Types
- `W3DTerrainLogic` (Class): Main terrain logic handler for W3D rendering
- `WorldHeightMap` (Class): Temporary object for loading heightmap data
- `Region3D` (Struct): Used for storing terrain extents
- `Coord3D` (Struct): 3D coordinate representation

## Key Functions
### `loadMap`
- Purpose: Loads terrain data from a map file
- Calls: `WorldHeightMap` constructor, `TerrainLogic::loadMap`, `TheGameClient->setTimeOfDay`

### `getGroundHeight`
- Purpose: Returns the terrain height at given coordinates
- Calls: `TheTerrainRenderObject->getHeightMapHeight`

### `getLayerHeight`
- Purpose: Returns height considering terrain layers (ground/walls/bridges)
- Calls: `TheTerrainRenderObject->getHeightMapHeight`, `TheAI->pathfinder()->isPointOnWall`, `findBridgeLayerAt`

### `isClearLineOfSight`
- Purpose: Checks if line of sight exists between two points
- Calls: `TheTerrainRenderObject->isClearLineOfSight`

## Globals
- `TheTerrainRenderObject` (External): Access to terrain rendering functionality
- `TheAI` (External): Access to AI pathfinding
- `TheMapCache` (External): Map caching system
- `TheGlobalData`/`TheWritableGlobalData` (External): Game global data

## Dependencies
- `W3DTerrainLogic.h` (header)
- `HeightMap.h`, `WorldHeightMap.h` (terrain data)
- `GameClient.h` (client interface)
- `AI.h`, `AIPathfind.h` (pathfinding)
- `MapUtil.h` (map utilities)
- `Xfer.h` (serialization)
- `GlobalData.h` (game globals)
