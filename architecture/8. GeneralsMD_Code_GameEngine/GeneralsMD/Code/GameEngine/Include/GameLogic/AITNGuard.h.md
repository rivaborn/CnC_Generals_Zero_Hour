# GeneralsMD/Code/GameEngine/Include/GameLogic/AITNGuard.h

## Purpose
Defines AI state machine classes for tunnel network guard behavior in Command & Conquer Generals.

## Responsibilities
- Defines guard states for AI units
- Manages tunnel network exit conditions
- Implements state machine for guard behavior
- Handles guard modes and target tracking

## Key Types
- TunnelNetworkExitConditions (Class): exit condition logic for attacks
- AITNGuardMachine (Class): main state machine for guard behavior
- AITNGuardInnerState (Class): state for attacking within inner area
- AITNGuardIdleState (Class): state for waiting for targets
- AITNGuardOuterState (Class): state for attacking aggressive targets
- AITNGuardReturnState (Class): state for returning to guard position
- AITNGuardPickUpCrateState (Class): state for picking up crates
- AITNGuardAttackAggressorState (Class): state for attacking aggressors

## Key Functions
### TunnelNetworkExitConditions::shouldExit
- Purpose: Determines if attack should exit
- Calls: Not inferable

### AITNGuardMachine::lookForInnerTarget
- Purpose: Scans for enemy targets within guard range
- Calls: Not inferable

### AITNGuardInnerState::onEnter
- Purpose: Initializes inner guard state
- Calls: Not inferable

### AITNGuardInnerState::update
- Purpose: Updates inner guard state logic
- Calls: Not inferable

### AITNGuardInnerState::onExit
- Purpose: Cleans up inner guard state
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/GameMemory.h
- GameLogic/AIStateMachine.h
- GameLogic/GameLogic.h
- GameLogic/Object.h
- GameLogic/AI.h
