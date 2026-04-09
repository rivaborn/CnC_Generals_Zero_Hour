# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/HighlanderBody.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized damage-handling component for objects that should resist death from normal damage (e.g., certain buildings or units). It extends the game's damage system by overriding `attemptDamage` to enforce a "last hitpoint" rule, critical for game balance and special unit behaviors.

## Cross-References
### Incoming
- Damage system (via `DamageInfo` calls)
- Network serialization (via `Xfer` calls)
- Object lifecycle (via `Thing` and `ActiveBody` usage)

### Outgoing
- `ActiveBody` (base class for damage handling)
- `Xfer` (for network sync)
- `DamageInfo` (for damage processing)

## Design Patterns
- **Template Method**: Extends `ActiveBody` by overriding `attemptDamage` while delegating to parent for core logic.
- **Strategy**: Encapsulates damage resistance as a modular behavior that can be swapped (e.g., for different unit types).
- **Null Object**: Empty destructor suggests lightweight, stateless design for composition.

*Not inferable*: No clear use of Observer or Factory patterns in this snippet.
