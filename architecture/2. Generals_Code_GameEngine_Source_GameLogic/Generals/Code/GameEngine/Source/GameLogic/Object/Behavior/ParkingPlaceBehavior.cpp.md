# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/ParkingPlaceBehavior.cpp

## Purpose
This file implements the `ParkingPlaceBehavior` class, which manages parking spaces and runways for objects in the game, including handling reservations, object placement, and healing.

## Responsibilities
- Manage parking spaces and runways for objects.
- Handle reservations for parking spaces and runways.
- Place objects in designated parking spaces or runways.
- Heal objects within reserved spaces.
- Ensure proper cleanup of dead objects from parking spaces.

## Key Types
- `ParkingPlaceBehavior` (Class): Manages parking spaces and runways.
- `ParkingPlaceInfo` (Struct): Stores information about a parking space.
- `RunwayInfo` (Struct): Stores information about a runway.
- `HealingInfo` (Struct): Stores information about healing objects.

## Key Functions
### buildInfo
- Purpose: Initializes parking spaces and runways based on module data.
- Calls: 
  - `getObject()->testStatus`
  - `getParkingPlaceBehaviorModuleData()`
  - `getObject()->getProductionUpdateInterface()`
  - `getObject()->getSingleLogicalBonePosition`

### reserveSpace
- Purpose: Reserves a parking space for an object and provides parking information.
- Calls:
  - `buildInfo()`
  - `purgeDead()`
  - `findPPI()`
  - `findEmptyPPI()`
  - `getObject()->getProductionUpdateInterface()->setHoldDoorOpen`

### releaseSpace
- Purpose: Releases a reserved parking space for an object.
- Calls:
  - `buildInfo()`
  - `purgeDead()`
  - `getObject()->getProductionUpdateInterface()->setHoldDoorOpen`

### exitObjectViaDoor
- Purpose: Moves an object to a designated parking space or runway and sets its position and orientation.
- Calls:
  - `buildInfo()`
  - `purgeDead()`
  - `findEmptyPPI()`
  - `getObject()->getSingleLogicalBonePosition`
  - `newObj->setPosition`
  - `newObj->setOrientation`
  - `TheAI->pathfinder()->addObjectToPathfindMap`

## Globals
- `HEAL_RATE_FRAMES` (Int): Rate at which healing occurs.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/CRCDebug.h"
  - "Common/Xfer.h"
  - "GameLogic/AI.h"
  - "GameLogic/Module/ParkingPlaceBehavior.h"
  - "GameLogic/Object.h"
  - "GameLogic/TerrainLogic.h"

- External symbols used:
  - `TheGameLogic`
  - `TheAI`
  - `TheNameKeyGenerator`
