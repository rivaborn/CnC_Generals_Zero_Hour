# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PilotFindVehicleUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a specialized update module for handling wounded infantry behavior, specifically their search for healing vehicles or structures. It integrates into the game's modular update system, extending the base `UpdateModule` class to provide targeted AI logic for pilot units.

## Cross-References
### Incoming
- Likely called by the game's update loop or behavior manager (not explicitly shown in header)
- May be referenced by infantry unit templates that require healing behavior

### Outgoing
- Uses `ModuleData` for configuration parsing
- Interacts with `Thing` and `Object` for target scanning
- Depends on `UpdateModule` base class for update timing

## Design Patterns
- **Template Method Pattern**: Extends `UpdateModule` with specific behavior in `update()` and `onObjectCreated()`
- **Data-Driven Design**: Uses `ModuleData` for configurable parameters (scan range, health thresholds)
- **Memory Pool Pattern**: Uses `MEMORY_POOL_GLUE` for object allocation management

*Not inferable*: Exact scanning algorithm or healing target selection criteria.
