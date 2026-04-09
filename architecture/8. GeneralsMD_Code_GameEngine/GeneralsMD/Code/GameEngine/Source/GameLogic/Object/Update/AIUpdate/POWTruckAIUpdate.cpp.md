# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/POWTruckAIUpdate.cpp

## Purpose
Implements AI logic for the POW Truck unit in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages POW Truck behavior states (waiting, finding targets, collecting prisoners, returning prisoners)
- Handles prisoner pickup and return commands
- Tracks prison locations and validates targets
- Manages AI mode switching (automatic/manual)

## Key Types
- `POWTruckAIUpdateModuleData` (Class): Stores module configuration (boredom time, prison distance)
- `POWTruckAIUpdate` (Class): Main AI update class for POW Truck
- `POWTruckTask` (Enum): Represents truck states (WAITING, FIND_TARGET, COLLECTING_TARGET, RETURNING_PRISONERS)
- `POWTruckAIMode` (Enum): Represents AI control modes (AUTOMATIC, MANUAL)

## Key Functions
### `updateWaiting`
- Purpose: Handles truck behavior while waiting for commands
- Calls: `setTask`, `getPOWTruckAIUpdateModuleData`, `TheGameLogic->getFrame`

### `updateFindTarget`
- Purpose: Searches for valid prisoner targets when in automatic mode
- Calls: `validateTarget`, `isQuickPathAvailable`, `TheAI->pathfinder()->quickDoesPathExist`

### `loadPrisoner`
- Purpose: Adds a prisoner to the truck's containment
- Calls: `validateTarget`, `getContain`, `addToContain`, `setTask`

### `unloadPrisonersToPrison`
- Purpose: Transfers prisoners from truck to prison and handles bounty
- Calls: `getContain`, `iterateContained`, `deposit`, `addFloatingText`

### `findBestPrison`
- Purpose: Locates the closest prison for the truck
- Calls: `getProducerID`, `TheGameLogic->findObjectByID`

## Globals
- `FIND_DELAY` (const UnsignedInt): Delay between target search attempts

## Dependencies
- `AIUpdateInterface`, `Object`, `Player`, `ContainModuleInterface`
- `TheGameLogic`, `ThePartitionManager`, `TheAI`, `TheActionManager`
- `TheGlobalData`, `TheGameText`, `TheInGameUI`
