# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/SupplyWarehouseCripplingBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements a behavior module for supply warehouses, managing damage states, healing mechanics, and docking functionality. It integrates with the game's damage system and update loop, demonstrating the modular behavior architecture of the SAGE engine.

## Cross-References
### Incoming
- **Damage System**: Calls `onDamage` and `onBodyDamageStateChange` when damage occurs or state changes.
- **Update Loop**: Invokes `update` periodically for healing logic.
- **Docking System**: Uses `DockUpdateInterface` for crippled state management.

### Outgoing
- **Game Logic**: Accesses `TheGameLogic` for frame timing.
- **Body Module**: Queries health state via `getBodyModule()`.
- **Update Module**: Inherits from `UpdateModule` for sleep/wake mechanics.

## Design Patterns
- **State Pattern**: Manages different damage states (e.g., `BODY_REALLYDAMAGED`) with conditional behavior.
- **Timer-Based Update**: Uses `UpdateModule`'s sleep/wake system to optimize healing checks.
- **Data-Driven Configuration**: Healing parameters are parsed from INI files via `buildFieldParse`.
