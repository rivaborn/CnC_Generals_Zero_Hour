# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/ParkingPlaceBehavior.cpp

## Purpose
Manages parking spaces, runways, and healing for aircraft in structures like hangars and helipads.

## Responsibilities
- Tracks occupied/reserved parking spaces and runways
- Handles aircraft entry/exit via doors
- Manages healing for docked units
- Maintains rally points for helicopters
- Serializes/deserializes state for save games

## Key Types
- `ParkingPlaceBehavior` (Class): Main behavior class managing parking logic
- `ParkingPlaceInfo` (Struct): Stores data for individual parking spaces
- `RunwayInfo` (Struct): Tracks runway usage state
- `HealingInfo` (Struct): Manages healing state for docked units

## Key Functions
### `buildInfo()`
- Purpose: Initializes parking space and runway data from object bones
- Calls: `getObject()->getSingleLogicalBonePosition()`

### `purgeDead()`
- Purpose: Removes references to destroyed objects from tracking lists
- Calls: `TheGameLogic->findObjectByID()`

### `reserveSpace()`
- Purpose: Allocates a parking space for an aircraft
- Calls: `findPPI()`, `findEmptyPPI()`, `calcPPInfo()`

### `exitObjectViaDoor()`
- Purpose: Handles aircraft exiting through a door
- Calls: `reserveSpace()`, `ai->aiFollowExitProductionPath()`

### `update()`
- Purpose: Handles periodic healing and runway management
- Calls: `TheGameLogic->findObjectByID()`, `body->attemptHealing()`

## Globals
- `HEAL_RATE_FRAMES` (Int): Number of frames between healing updates

## Dependencies
- `UpdateModule.h`, `ParkingPlaceBehavior.h`, `AI.h`, `GameLogic.h`
- `Xfer.h` for serialization
- `TheGameLogic`, `TheNameKeyGenerator` global instances
