# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIGuard.cpp

## Purpose
Implements AI guard behavior for units, managing states like patrolling, attacking intruders, and returning to guard positions.

## Responsibilities
- Manages guard state machine with states for idle, inner/outer guard, return, and attack
- Handles target acquisition and attack logic for guarded areas/objects
- Implements exit conditions for guard states (time, distance, target loss)
- Coordinates with pathfinding and team targeting systems

## Key Types
- `AIGuardMachine` (Class): Main guard state machine controller
- `ExitConditions` (Class): Manages conditions for exiting guard states
- `AIGuardInnerState` (Class): State for close-range guarding
- `AIGuardOuterState` (Class): State for long-range guarding
- `AIGuardReturnState` (Class): State for returning to guard position
- `AIGuardIdleState` (Class): State for idle guarding
- `AIGuardPickUpCrateState` (Class): State for crate pickup during guard
- `AIGuardAttackAggressorState` (Class): State for attacking aggressors

## Key Functions
### `hasAttackedMeAndICanReturnFire`
- Purpose: Checks if the unit can attack its last attacker
- Calls: `getClearableLastAttacker`, `findObjectByID`, `getRelationship`, `isAbleToAttack`, `getAbleToAttackSpecificObject`

### `lookForInnerTarget`
- Purpose: Finds closest valid target within guard range
- Calls: `getClosestObject`, `getStdGuardRange`, `setNemesisID`

### `ExitConditions::shouldExit`
- Purpose: Determines if guard state should exit based on conditions
- Calls: `getFrame`, `getGoalObject`, `getPosition`

## Globals
- `CLOSE_ENOUGH` (Real): Distance threshold constant (25.0f)

## Dependencies
- `AI.h`, `AIGuard.h`, `Object.h`, `PartitionManager.h`, `PolygonTrigger.h`
- `TheGameLogic`, `ThePartitionManager`, `TheTerrainLogic`, `TheAI`
- `StateMachine`, `AIUpdateInterface`, `BodyModuleInterface`
