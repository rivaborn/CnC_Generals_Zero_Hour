# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ProductionExitUpdate/SpawnPointProductionExitUpdate.cpp

## Purpose
Handles spawning units at named bone positions on a production structure.

## Responsibilities
- Manages spawn point positions via bone transforms
- Tracks occupancy of spawn points
- Places newly created units at available spawn points
- Ensures units are positioned on terrain

## Key Types
- `SpawnPointProductionExitUpdate` (Class): Production exit module that uses bone positions for spawning
- `SpawnPointProductionExitUpdateModuleData` (Struct): Module data containing bone name

## Key Functions
### `exitObjectViaDoor`
- Purpose: Places a new unit at an available spawn point
- Calls: `initializeBonePositions`, `TheTerrainLogic->getLayerHeight`, `TheAI->pathfinder()->addObjectToPathfindMap`

### `reserveDoorForExit`
- Purpose: Checks if a spawn point is available
- Calls: `initializeBonePositions`, `revalidateOccupiers`

### `initializeBonePositions`
- Purpose: Extracts spawn point positions from bone transforms
- Calls: `getPristineBonePositions`, `convertBonePosToWorldPos`

### `revalidateOccupiers`
- Purpose: Cleans up invalid object references in spawn points
- Calls: `TheGameLogic->findObjectByID`

## Globals
- `MAX_SPAWN_POINTS` (const): Maximum number of spawn points (not shown in code but used)

## Dependencies
- `UpdateModule`, `Thing`, `Object`, `Drawable`, `AI`, `GameLogic`, `TerrainLogic`
- `Xfer`, `Matrix3D`, `Coord3D`, `ThingTemplate`
