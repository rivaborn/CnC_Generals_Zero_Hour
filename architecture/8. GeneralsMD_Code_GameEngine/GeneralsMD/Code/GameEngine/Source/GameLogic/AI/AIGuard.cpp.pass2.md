# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIGuard.cpp - Enhanced Analysis

## Architectural Role
This file implements the guard behavior state machine for AI units, bridging the AI subsystem with game logic and team coordination. It handles dynamic guard state transitions based on environmental changes and unit interactions.

## Cross-References
### Incoming
- `AI.cpp` (uses guard states in behavior trees)
- `Team.cpp` (sets team targets during attacks)
- `Object.cpp` (queries relationships/attack capabilities)

### Outgoing
- `AIPathfind.cpp` (for movement during guard states)
- `PartitionManager.cpp` (spatial queries for targets)
- `BodyModule.cpp` (damage/attacker tracking)

## Design Patterns
- **State Pattern**: Guard behavior is decomposed into discrete states (Idle, Attack, Return) with clear transitions.
- **Strategy Pattern**: Exit conditions are encapsulated in `ExitConditions`, allowing dynamic evaluation without modifying state logic.
- **Observer Pattern**: Reacts to damage events via `getLastDamageInfo()` to trigger aggressor attacks.

*Not inferable*: Exact event dispatch mechanism for damage notifications.
