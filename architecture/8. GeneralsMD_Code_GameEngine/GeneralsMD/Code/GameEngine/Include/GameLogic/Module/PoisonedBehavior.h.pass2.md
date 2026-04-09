# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PoisonedBehavior.h - Enhanced Analysis

## Architectural Role
This file implements the poison damage system, a key game mechanic that applies continuous damage over time. It bridges the damage system with the update loop, demonstrating how modular behaviors are composed in the SAGE engine.

## Cross-References
### Incoming
- Damage application logic (e.g., from weapon effects)
- Thing update system (game loop)
- Modding system (via `buildFieldParse`)

### Outgoing
- DamageModule interface for damage handling
- UpdateModule for periodic updates
- Thing system for state management

## Design Patterns
- **Strategy Pattern**: Poison behavior is modular and can be attached to any Thing via the BehaviorModule system.
- **Observer Pattern**: Reacts to damage events via `onDamage` and `onHealing`.
- **State Machine**: Manages poisoned state transitions implicitly through `startPoisonedEffects`/`stopPoisonedEffects`.

*(Token count: 198)*
