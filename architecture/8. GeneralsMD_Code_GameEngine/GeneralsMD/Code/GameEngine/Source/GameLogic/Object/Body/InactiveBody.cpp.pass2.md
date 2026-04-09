# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/InactiveBody.cpp - Enhanced Analysis

## Architectural Role
This file implements the `InactiveBody` module, which serves as a lightweight body component for objects that don't require health/damage mechanics (e.g., prerequisites). It integrates with the game's damage system while bypassing health-related logic, demonstrating the engine's modular design for object behavior.

## Cross-References
### Incoming
- **Damage System**: Calls `attemptDamage()` and `attemptHealing()` when processing damage/healing events.
- **Object Lifecycle**: Invoked during object creation (constructor) and destruction (`onDie()`).
- **Serialization**: Used by `Xfer` system for save/load operations.

### Outgoing
- **BodyModule**: Inherits and extends base functionality (e.g., `crc()`, `xfer()`).
- **DieModule**: Triggers `onDie()` for `DAMAGE_UNRESISTABLE` cases.
- **Object**: Manages object state via `setEffectivelyDead()` and `onDie()`.

## Design Patterns
- **Null Object Pattern**: Represents objects without health/damage, delegating to base class where applicable.
- **Strategy Pattern**: Implements damage handling as a strategy (no effect by default, except for `DAMAGE_UNRESISTABLE`).
- **Template Method**: Overrides `BodyModule` methods to provide no-op behavior (e.g., `internalChangeHealth()`).
