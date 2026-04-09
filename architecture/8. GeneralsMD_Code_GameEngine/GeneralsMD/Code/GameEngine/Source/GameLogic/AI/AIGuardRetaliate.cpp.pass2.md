# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIGuardRetaliate.cpp - Enhanced Analysis

## Architectural Role
This file implements the AI's guard retaliation system, a key component of the behavior tree that handles unit responses to attacks. It bridges the AI decision-making with the game's combat logic, managing state transitions for units when they need to retaliate against aggressors.

## Cross-References
### Incoming
- Called by AI behavior tree nodes when units need to retaliate
- Used by damage/attack systems to trigger guard responses
- Referenced by team coordination logic for shared targets

### Outgoing
- Calls into `AI.h` for pathfinding and target acquisition
- Uses `GameLogic.h` for object relationships and state queries
- Interfaces with `PartitionManager.h` for spatial queries
- Depends on `BodyModuleInterface` for damage tracking

## Design Patterns
- **State Machine**: Uses hierarchical state machine for guard behavior (e.g., `AIGuardRetaliateAttackAggressorState`)
- **Strategy Pattern**: Exit conditions are encapsulated in `GuardRetaliateExitConditions`
- **Observer Pattern**: Reacts to damage events via `BodyModuleInterface`'s last attacker tracking

*Not inferable*: Exact event-driven integration with damage system.
