# GeneralsMD/Code/GameEngine/Include/GameLogic/AIDock.h

## Purpose
Defines the AI docking state machine and its associated states for managing unit docking behavior.

## Responsibilities
- Declares docking state machine and states
- Defines docking state transitions
- Manages docking approach, clearance, processing, and exit
- Handles drone repair during docking

## Key Types
- AIDockMachine (Class): Main docking state machine
- AIDockApproachState (Class): State for moving to approach position
- AIDockWaitForClearanceState (Class): State for waiting for dock clearance
- AIDockAdvancePositionState (Class): State for advancing in line
- AIDockMoveToEntryState (Class): State for moving to dock entrance
- AIDockMoveToDockState (Class): State for moving to dock position
- AIDockProcessDockState (Class): State for processing dock actions
- AIDockMoveToExitState (Class): State for moving to dock exit
- AIDockMoveToRallyState (Class): State for moving to rally point
- AI_DOCK_APPROACH (Enum): Docking state enum values

## Key Functions
### AIDockMachine::ableToAdvance
- Purpose: Checks if unit can advance in docking queue
- Calls: Not inferable

### AIDockMachine::halt
- Purpose: Stops the docking state machine
- Calls: Not inferable

### AIDockProcessDockState::setNextDockActionFrame
- Purpose: Sets delay between dock action calls
- Calls: Not inferable

### AIDockProcessDockState::findMyDrone
- Purpose: Finds associated drone for repair
- Calls: Not inferable

## Globals
None

## Dependencies
- Common/GameMemory.h
- GameLogic/AIStateMachine.h
- StateMachine, AIInternalMoveToState, State, Xfer classes
- MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE macro
