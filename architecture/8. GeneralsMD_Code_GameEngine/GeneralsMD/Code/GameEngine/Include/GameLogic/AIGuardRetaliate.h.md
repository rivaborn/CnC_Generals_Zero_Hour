# GeneralsMD/Code/GameEngine/Include/GameLogic/AIGuardRetaliate.h

## Purpose
Defines AI state machine and states for unit guard/retaliation behavior in Command & Conquer Generals.

## Responsibilities
- Declares guard retaliation state machine and its states
- Defines exit conditions for attack states
- Manages guard position and nemesis targeting
- Handles crate pickup and aggressor attack logic

## Key Types
- **GuardRetaliateExitConditions (Class)**: Attack exit condition evaluator
- **AIGuardRetaliateMachine (Class)**: Main guard retaliation state machine
- **AIGuardRetaliateInnerState (Class)**: Inner guard attack state
- **AIGuardRetaliateIdleState (Class)**: Idle waiting state
- **AIGuardRetaliateOuterState (Class)**: Outer area attack state
- **AIGuardRetaliateReturnState (Class)**: Return to guard position state
- **AIGuardRetaliatePickUpCrateState (Class)**: Crate pickup state
- **AIGuardRetaliateAttackAggressorState (Class)**: Aggressor attack state
- **ExitConditionsEnum (Enum)**: Exit condition flags

## Key Functions
### `shouldExit`
- Purpose: Evaluates whether attack state should exit
- Calls: Not inferable

### `lookForInnerTarget`
- Purpose: Finds targets within inner guard radius
- Calls: Not inferable

### `getStdGuardRange`
- Purpose: Gets standard guard range for an object
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/GameMemory.h`
- `GameLogic/AIStateMachine.h`
- `GameLogic/GameLogic.h`
- `GameLogic/Object.h`
- `GameLogic/AI.h`
