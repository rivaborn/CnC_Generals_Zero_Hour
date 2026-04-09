# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ProductionExitUpdate/SpawnPointProductionExitUpdate.cpp

## Purpose
This file implements the `SpawnPointProductionExitUpdate` class, which handles the spawning and positioning of units at specific bone locations on a game object.

## Responsibilities
- Initialize spawn point positions based on bone data.
- Reserve and unreserve exit points for unit production.
- Position newly created units at designated spawn points.
- Update and validate occupier status of spawn points.

## Key Types
- `SpawnPointProductionExitUpdate` (Class): Manages unit spawning at specific locations on an object.
- None

## Key Functions
### SpawnPointProductionExitUpdate::exitObjectViaDoor
- Purpose: Positions a newly created unit at a designated spawn point and updates its orientation and layer.
- Calls:
  - `initializeBonePositions`
  - `TheTerrainLogic->getLayerHeight`
  - `newObj->setPosition`
  - `newObj->setOrientation`
  - `newObj->setLayer`
  - `TheAI->pathfinder()->addObjectToPathfindMap`
  - `newObj->setDisabled`

### SpawnPointProductionExitUpdate::reserveDoorForExit
- Purpose: Reserves a spawn point for unit production.
- Calls:
  - `initializeBonePositions`
  - `revalidateOccupiers`

### SpawnPointProductionExitUpdate::unreserveDoorForExit
- Purpose: Unreserves a previously reserved spawn point.
- Calls: None

### SpawnPointProductionExitUpdate::initializeBonePositions
- Purpose: Initializes the world positions and angles of spawn points based on bone data.
- Calls:
  - `getObject()->getDrawable()`
  - `myDrawable->getPristineBonePositions`
  - `me->convertBonePosToWorldPos`

### SpawnPointProductionExitUpdate::revalidateOccupiers
- Purpose: Validates the occupier status of spawn points by checking if the objects still exist.
- Calls:
  - `TheGameLogic->findObjectByID`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/AI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/Module/SpawnPointProductionExitUpdate.h"
  - "WWMath/Matrix3D.h"

- External symbols used:
  - `TheTerrainLogic`
  - `TheAI`
  - `TheGameLogic`
