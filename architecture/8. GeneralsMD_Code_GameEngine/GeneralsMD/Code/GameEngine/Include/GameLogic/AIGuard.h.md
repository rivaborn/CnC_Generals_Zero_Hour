# GeneralsMD/Code/GameEngine/Include/GameLogic/AIGuard.h

## Purpose
Defines AI guard states and behavior for units in Command & Conquer Generals.

## Responsibilities
- Declares state machine classes for guard behavior
- Defines guard state enums and exit conditions
- Manages transitions between guard states
- Handles target selection and attack logic

## Key Types
- **ExitConditions (Class)**: Manages conditions for exiting attack states
- **AIGuardMachine (Class)**: Base state machine for guard behavior
- **AIGuardInnerState (Class)**: State for attacking within inner guard radius
- **AIGuardIdleState (Class)**: State for waiting when no threats are present
- **AIGuardOuterState (Class)**: State for attacking aggressive units in outer radius
- **AIGuardReturnState (Class)**: State for returning to guard position
- **AIGuardPickUpCrateState (Class)**: State for picking up supply crates
- **AIGuardAttackAggressorState (Class)**: State for attacking specific aggressors

## Key Functions
### `ExitConditions::shouldExit`
- Purpose: Determines if attack state should exit based on conditions
- Calls: Not inferable

### `AIGuardMachine::lookForInnerTarget`
- Purpose: Finds targets within inner guard radius
- Calls: Not inferable

### `AIGuardInnerState::onEnter`
- Purpose: Initializes inner guard state behavior
- Calls: Not inferable

### `AIGuardIdleState::update`
- Purpose: Updates idle guard state logic
- Calls: Not inferable

## Globals
- None

## Dependencies
- `AIStateMachine.h` (StateMachine, State)
- `GameLogic.h` (GuardMode)
- `Object.h` (ObjectID)
- `AI.h` (AIAttackState, AIEnterState, AIPickUpCrateState)
- `Common/GameMemory.h` (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
