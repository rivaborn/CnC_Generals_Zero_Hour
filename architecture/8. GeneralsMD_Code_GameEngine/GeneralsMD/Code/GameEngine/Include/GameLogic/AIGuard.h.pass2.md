# GeneralsMD/Code/GameEngine/Include/GameLogic/AIGuard.h - Enhanced Analysis

## Architectural Role
This file defines the AI guard behavior system, a critical component of the game's tactical AI. It implements a state machine pattern to manage unit guarding logic, integrating with the broader AI framework and object system.

## Cross-References
### Incoming
- AI state machine controller (likely in `AI.h`)
- Object behavior system (via `Object.h`)
- Game logic manager (`TheGameLogic`)

### Outgoing
- `AIStateMachine.h` (base state machine classes)
- `GameLogic.h` (guard mode definitions)
- `AI.h` (attack/enter/pickup state implementations)
- `Common/GameMemory.h` (memory management macros)

## Design Patterns
- **State Pattern**: Used extensively to model different guard behaviors (idle, attack, return, etc.)
- **Strategy Pattern**: Exit conditions are encapsulated in `ExitConditions` class, allowing dynamic behavior configuration
- **Composite Pattern**: Guard states contain nested attack/enter states (e.g., `AIGuardInnerState` contains `AIAttackState`)

*Not inferable*: Exact implementation of state transitions or memory pool usage details.
