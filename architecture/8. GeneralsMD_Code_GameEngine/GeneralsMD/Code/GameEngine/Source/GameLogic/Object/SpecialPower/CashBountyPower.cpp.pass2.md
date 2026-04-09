# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashBountyPower.cpp - Enhanced Analysis

## Architectural Role
This file implements the cash bounty system, a game mechanic where destroying enemy units grants the player in-game currency. It bridges the gap between unit destruction events and player resource management, ensuring bounty values are calculated and applied correctly.

## Cross-References
### Incoming
- **GameLogic/Module/CashBountyPower.h**: Defines the module data and class interfaces used here.
- **Common/Player.h**: Provides player-related functions like `getCashBounty()` and `setCashBounty()`.
- **GameLogic/Object.h**: Used for `getObject()` and `getControllingPlayer()` calls.

### Outgoing
- **SpecialPowerModule**: Base class for special power logic (inheritance).
- **Common/Xfer.h**: Handles serialization/deserialization for networking.
- **INI parsing utilities**: For configuration (commented-out upgrade system).

## Design Patterns
- **Template Method**: `onSpecialPowerCreation()` extends base class behavior.
- **Strategy**: Bounty calculation logic is encapsulated in `findBounty()`.
- **Observer**: Reacts to object creation/destruction events (via `onObjectCreated`).

*Not inferable*: Exact INI parsing pattern (commented-out code).
