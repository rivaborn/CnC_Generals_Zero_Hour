# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/POWTruckAIUpdate.h

## Purpose
Defines AI logic for the POW Truck unit in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages POW Truck AI state machine
- Handles prisoner collection and transport
- Implements automatic and manual AI modes
- Provides interface for external AI commands

## Key Types
- `POWTruckAIUpdateModuleData` (Class): Configuration data for POW Truck AI
- `POWTruckTask` (Enum): AI task states (WAITING, FIND_TARGET, COLLECTING_TARGET, RETURNING_PRISONERS)
- `POWTruckAIUpdateInterface` (Class): Virtual interface for POW Truck AI commands
- `POWTruckAIUpdate` (Class): Main AI update implementation for POW Truck
- `POWTruckAIMode` (Enum): AI control modes (AUTOMATIC, MANUAL)

## Key Functions
### `updateWaiting`
- Purpose: Handles AI logic when truck is waiting
- Calls: Not inferable

### `updateFindTarget`
- Purpose: Handles AI logic when searching for prisoners
- Calls: Not inferable

### `updateCollectingTarget`
- Purpose: Handles AI logic when collecting a prisoner
- Calls: Not inferable

### `updateReturnPrisoners`
- Purpose: Handles AI logic when returning prisoners to base
- Calls: Not inferable

### `validateTarget`
- Purpose: Checks if a target is valid for collection
- Calls: Not inferable

### `findBestPrison`
- Purpose: Locates the optimal prison for unloading
- Calls: Not inferable

### `findBestTarget`
- Purpose: Locates the optimal prisoner to collect
- Calls: Not inferable

## Globals
- None

##
