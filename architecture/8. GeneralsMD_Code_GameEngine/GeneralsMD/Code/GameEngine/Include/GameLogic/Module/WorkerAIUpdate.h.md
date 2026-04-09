# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WorkerAIUpdate.h

## Purpose
Defines the AI logic for worker units that combine dozer and supply truck behaviors in Command & Conquer Generals.

## Responsibilities
- Manages worker state transitions between dozer and supply truck modes
- Handles construction, repair, and supply delivery tasks
- Maintains task queues and dock point information
- Controls audio events for building and supply operations

## Key Types
- **WorkerStateMachine (Class)**: Manages state transitions between dozer and supply truck behaviors
- **WorkerAIUpdateModuleData (Class)**: Contains configurable parameters for worker AI behavior
- **WorkerAIInterface (Class)**: Interface for worker-specific AI commands
- **WorkerAIUpdate (Class)**: Main AI controller for worker units
- **DozerTaskInfo (Class)**: Stores task information for dozer operations
- **DozerDockPointInfo (Class)**: Stores dock point information for construction tasks

## Key Functions
### `update()`
- Purpose: Main update function for worker AI
- Calls: State machine updates, task management functions

### `aiDoCommand()`
- Purpose: Handles player-issued commands for the worker
- Calls: Task management and state transition functions

### `privateRepair()`
- Purpose: Performs repair operations on target objects
- Calls: Not inferable from header

### `privateResumeConstruction()`
- Purpose: Resumes construction on target objects
- Calls: Not inferable from header

## Globals
- **m_suppliesDepletedVoice (AudioEventRTS)**: Sound played when taking the last supply box

## Dependencies
- `Common/StateMachine.h`
- `GameLogic/Module/AIUpdate.h`
- `GameLogic/Module/DozerAIUpdate.h`
- `GameLogic/Module/SupplyTruckAIUpdate.h`
