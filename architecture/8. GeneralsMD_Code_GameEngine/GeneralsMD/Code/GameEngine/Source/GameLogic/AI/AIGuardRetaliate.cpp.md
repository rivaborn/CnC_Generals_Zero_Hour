# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIGuardRetaliate.cpp

## Purpose
Implements AI guard retaliation behavior, handling unit responses to attacks and target pursuit within defined guard ranges.

## Responsibilities
- Manages state machine for guard retaliation logic
- Handles target acquisition and attack conditions
- Implements guard range calculations and exit conditions
- Manages crate pickup during guard states
- Coordinates team-wide target selection

## Key Types
- `AIGuardRetaliateMachine` (Class): Main state machine for guard retaliation
- `GuardRetaliateExitConditions` (Class): Exit condition evaluator for guard states
- `AIGuardRetaliateAttackAggressorState` (Class): State for attacking aggressors
- `AIGuardRetaliateInnerState` (Class): State for close-range attacks
- `AIGuardRetaliateOuterState` (Class): State for long-range attacks

## Key Functions
### `hasAttackedMeAndICanReturnFire`
- Purpose: Checks if unit can retaliate against last attacker
- Calls: `getClearableLastAttacker`, `findObjectByID`, `getRelationship`, `isAbleToAttack`, `getAbleToAttackSpecificObject`

### `lookForInnerTarget`
- Purpose: Finds closest attackable enemy within guard range
- Calls: `getClosestObject`, `setNemesisID`

### `GuardRetaliateExitConditions::shouldExit`
- Purpose: Evaluates exit conditions for guard states
- Calls: `getFrame`, `getPosition`, `lengthSqr`

## Globals
- `CLOSE_ENOUGH` (Real): Distance threshold constant (25.0f)

## Dependencies
- `AI.h`, `AIGuardRetaliate.h`, `PartitionManager.h`, `GameLogic.h`
- `StateMachine`, `Object`, `Team`, `BodyModuleInterface`
- `TheGameLogic`, `ThePartitionManager`, `TheAI`
