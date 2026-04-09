# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BunkerBusterBehavior.h - Enhanced Analysis

## Architectural Role
This file defines a behavior module for bunker destruction, integrating with the game's module system (BehaviorModule, UpdateModule, DieModule). It handles special weapon effects (shockwaves, occupant damage) and upgrade-dependent functionality, bridging weapon systems and object interaction logic.

## Cross-References
### Incoming
- **Weapon systems**: Likely called by weapon impact handlers when bunker-buster weapons hit targets
- **Object interaction**: Triggered by garrisoned unit logic when containers are destroyed
- **Upgrade system**: Referenced when checking for required upgrades

### Outgoing
- **FXList**: For playing detonation/crash-through effects
- **WeaponTemplate**: For shockwave/occupant damage effects
- **DieModuleInterface**: For death event handling
- **UpdateModule**: For periodic behavior updates

## Design Patterns
- **Strategy Pattern**: Encapsulates bunker destruction logic as a reusable module
- **Observer Pattern**: Reacts to object death events via DieModuleInterface
- **Template Method**: Uses MAKE_STANDARD_MODULE_MACRO for consistent module initialization

*Not inferable*: Exact relationship with garrisoned unit ejection logic.
