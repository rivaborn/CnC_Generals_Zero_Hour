# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIDock.cpp

## Purpose
Implements docking behavior for AI units in the game, managing state transitions for approaching, waiting, docking, and exiting docks.

## Responsibilities
- Manages state machine for docking behavior
- Handles communication with dock objects via `DockUpdateInterface`
- Implements queue management for multiple units waiting to dock
- Manages drone attachment/detachment during docking
- Provides state-specific movement and obstacle handling

## Key Types
- `AIDockMachine` (Class): State machine managing docking behavior
- `DroneInfo` (Struct): Helper struct for drone lookup during docking
- `AIDockApproachState` (Class): State for approaching dock waiting position
- `AIDockWaitForClearanceState` (Class): State for waiting in dock queue
- `AIDockProcessDockState` (Class): State for actual docking and processing

## Key Functions
### `findDrone`
- Purpose: Callback function to find a drone object owned by a specific unit
- Calls: None (callback for `iterateObjects`)

### `AIDockProcessDockState::findMyDrone`
- Purpose: Locates the drone associated with the docking unit
- Calls: `TheGameLogic->findObjectByID`, `player->iterateObjects`

### `AIDockMachine::ableToAdvance`
- Purpose: Determines if unit can advance in dock queue
- Calls: `dock->isClearToAdvance`

## Globals
- None

## Dependencies
- `Common/Module.h`, `Common/Player.h`
- `GameLogic/Object.h`, `GameLogic/AIDock.h`
- `GameLogic/Module/AIUpdate.h`
- `GameLogic/Module/SupplyTruckAIUpdate.h`
- `GameLogic/Module/UpdateModule.h`
- `StateMachine`, `DockUpdateInterface`, `AIUpdateInterface`
