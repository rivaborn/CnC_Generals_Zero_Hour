# GeneralsMD/Code/GameEngine/Include/GameLogic/AIGuardRetaliate.h - Enhanced Analysis

## Architectural Role
This file defines the AI state machine for guard/retaliation behavior, a core tactical component in the game's AI system. It implements the decision logic for units to defend positions, attack aggressors, and manage guard zones, directly influencing unit behavior during combat scenarios.

## Cross-References
### Incoming
- AI state machine controller (likely in `AI.h`)
- Unit behavior system (calls `lookForInnerTarget`, `getStdGuardRange`)
- Attack state management (uses `GuardRetaliateExitConditions`)

### Outgoing
- `AIStateMachine.h` (inherits `StateMachine`, `State`)
- `AI.h` (uses `AIAttackState`, `AIEnterState`, `AIInternalMoveToState`, `AIPickUpCrateState`)
- `Object.h` (interacts with game objects via `ObjectID`)

## Design Patterns
- **State Pattern**: Implements guard behavior as discrete states (Idle, Inner/Outer Attack, Return, etc.) for modular behavior switching.
- **Strategy Pattern**: `GuardRetaliateExitConditions` encapsulates exit condition logic, allowing dynamic evaluation of when to leave attack states.
- **Composite State Machine**: Nested states (e.g., `AIAttackState` within `AIGuardRetaliateInnerState`) for hierarchical behavior control.
