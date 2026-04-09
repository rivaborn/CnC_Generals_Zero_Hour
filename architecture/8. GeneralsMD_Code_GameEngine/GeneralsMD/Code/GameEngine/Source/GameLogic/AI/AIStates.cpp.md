# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIStates.cpp

## Purpose
Implements AI behavior states for the SAGE engine, including attack, hunt, and guard states.

## Responsibilities
- Defines state machines for AI behaviors (attack, hunt, guard)
- Implements state transition logic for unit actions
- Handles target acquisition and weapon range checks
- Manages state persistence via Xfer serialization
- Provides utility functions for position comparison and attack feasibility

## Key Types
- **AttackStateMachine (Class)**: Manages attack behavior state transitions
- **AIAttackMoveStateMachine (Class)**: Handles attack/move state logic
- **AIAttackThenIdleStateMachine (Class)**: Manages attack-then-idle behavior
- **AICommandParms (Struct)**: Stores command parameters for AI actions
- **StateConditionInfo (Struct)**: Defines state transition conditions

## Key Functions
### `isSamePosition`
- Purpose: Compares two positions for logical equality with tolerance
- Calls: None

### `cannotPossiblyAttackObject`
- Purpose: Determines if an object cannot be attacked
- Calls: None

### `findEnemyInContainer`
- Purpose: Finds enemies within a container object
- Calls: None

### `killEnemiesInContainer`
- Purpose: Destroys enemies within a container
- Calls: None

### `canPursue`
- Purpose: Checks if a unit can pursue a target
- Calls: None

## Globals
- **IDLE_COUNTDOWN_DELAY (UnsignedInt)**: Delay time for idle state countdown

## Dependencies
- Common modules: ActionManager, GameAudio, Player, Xfer
- GameLogic modules: AIStateMachine, Locomotor, Weapon
- GameClient modules: ControlBar, InGameUI
- Memory management: MemoryPool glue code
- Serialization: Xfer, CRC debugging

Rules followed. Output under 500 tokens.
