# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/FireWeaponWhenDeadBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized behavior module for objects that fire a weapon upon death, integrating with the game's upgrade and damage systems. It extends the `BehaviorModule` and `UpgradeMux` classes, demonstrating the engine's modular behavior architecture.

## Cross-References
### Incoming
- Called by object death event handlers (e.g., `onDie` callbacks in `Thing` or `Object` classes)
- Referenced in upgrade system for activation/deactivation logic

### Outgoing
- Calls into `WeaponStore` for weapon creation/firing
- Uses `UpgradeMux` for upgrade compatibility checks
- Accesses `Object` and `Player` for state queries

## Design Patterns
- **Strategy Pattern**: Encapsulates death behavior as a modular strategy (via `BehaviorModule`)
- **Observer Pattern**: Reacts to death events via `onDie` callback
- **Template Method**: Extends base class methods (`crc`, `xfer`, `loadPostProcess`) with specialized logic

*Not inferable*: Exact upgrade conflict resolution mechanism or weapon firing timing.
