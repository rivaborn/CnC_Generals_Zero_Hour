# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GrantStealthBehavior.h - Enhanced Analysis

## Architectural Role
This file defines a behavior module that integrates into the game's stealth system, specifically handling permanent stealth grants. It works within the modular behavior system, extending `UpdateModule` to provide time-based stealth application logic.

## Cross-References
### Incoming
- **BehaviorModule.h**: Uses `BehaviorModule` as base for module registration
- **UpdateModule.h**: Inherits from `UpdateModule` for periodic updates
- **UpgradeModule.h**: Likely used for stealth-related upgrades (inferred from include)
- **DamageModule.h**: May interact with damage systems for stealth-breaking mechanics

### Outgoing
- **ParticleSys.h**: Creates/manages particle effects for visual feedback
- **Common/BitFlagsIO.h**: Uses bitmask parsing for `KindOf` filtering

## Design Patterns
- **Module Pattern**: Extends `UpdateModule` for composable behavior
- **Data-Driven Design**: Uses `buildFieldParse` for INI configuration
- **Observer Pattern**: Likely notifies other systems when stealth is granted (inferred from behavior module architecture)

*Not inferable*: Exact stealth application mechanism or event-driven interactions.
