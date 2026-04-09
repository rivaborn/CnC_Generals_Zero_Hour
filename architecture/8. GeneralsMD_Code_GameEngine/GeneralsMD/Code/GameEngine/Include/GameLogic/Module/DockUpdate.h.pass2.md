# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DockUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core docking behavior system in the SAGE engine, serving as an abstract base class for all docking interactions. It manages the state machine for docking units (approach, enter, dock, exit) and coordinates with the game's pathfinding and object management systems.

## Cross-References
### Incoming
- `RailedTransportDockUpdate.h` (implements `action()`)
- `PrisonDockUpdate.h` (implements `action()`)
- `RepairDockUpdate.h` (overrides `isRallyPointAfterDockType()`)
- `SupplyCenterDockUpdate.h` (overrides `action()` and `update()`)
- `SupplyWarehouseDockUpdate.h` (overrides `action()`, `onObjectCreated()`, and `setDockCrippled()`)

### Outgoing
- Calls into `UpdateModule` base class for module lifecycle
- Uses `INI` parsing for configuration
- Interacts with `Thing` and `Object` for docking targets

## Design Patterns
- **Template Method Pattern**: Defines skeleton docking behavior while deferring `action()` to subclasses
- **State Pattern**: Manages docking state transitions (approach â enter â dock â exit)
- **Strategy Pattern**: Different docking behaviors (repair, supply, prison) implemented via derived classes
