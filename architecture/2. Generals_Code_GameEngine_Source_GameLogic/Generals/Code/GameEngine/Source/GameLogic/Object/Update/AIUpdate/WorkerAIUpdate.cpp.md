# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/WorkerAIUpdate.cpp

## Purpose
This file contains the implementation of `WorkerAIUpdate`, which manages the AI behavior for worker units in Command & Conquer Generals. Workers can function as both dozers and supply trucks, handling tasks like construction, repair, and resource gathering.

## Responsibilities
- Manage state machines for dozer and supply truck behaviors.
- Handle construction, repair, and resource gathering tasks.
- Update worker status and perform necessary actions based on current state.
- Serialize and deserialize worker data for saving/loading game states.

## Key Types
- **AS_DOZER (Enum)**: Represents the dozer mode of a worker.
- **AS_SUPPLY_TRUCK (Enum)**: Represents the supply truck mode of a worker.
- **ActAsDozerState (Class)**: State class for managing dozer behavior.
- **ActAsSupplyTruckState (Class)**: State class for managing supply truck behavior.

## Key Functions
### WorkerAIUpdate::WorkerAIUpdate
- Purpose: Initializes the worker AI update with necessary state machines and data structures.
- Calls: `createMachines`

### WorkerAIUpdate::~WorkerAIUpdate
- Purpose: Cleans up allocated resources, including state machines.
- Calls: `deleteInstance` on state machines.

### WorkerAIUpdate::update
- Purpose: Updates the worker's state machine and handles tasks based on current mode (dozer or supply truck).
- Calls: `createMachines`, `updateStateMachine`

### WorkerAIUpdate::construct
- Purpose: Handles construction commands for workers, including validation of build location and creation of new objects.
- Calls: `isLocationLegalToBuild`, `newObject`

## Globals
- None

## Dependencies
- **Includes**: Various headers from the game engine, including action management, state machines, resource gathering, and audio handling.
