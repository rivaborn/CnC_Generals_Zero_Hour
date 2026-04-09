# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TransportContain.h - Enhanced Analysis

## Architectural Role
This file defines the core transport containment system, extending the base `OpenContain` module to handle vehicle-based unit transport (e.g., APCs carrying infantry). It manages capacity, exit behavior, and rider state transitions, serving as a critical link between unit movement and tactical gameplay.

## Cross-References
### Incoming
- **RailedTransportContain.h**: Overrides `isSpecificRiderFreeToExit()` and `onRemoving()` for specialized rail-based transport logic.
- **Other containment modules**: Likely called by unit spawning/despawning systems during transport operations.

### Outgoing
- **OpenContain.h**: Inherits base containment logic.
- **INI parsing system**: Uses `MultiIniFieldParse` for module data configuration.
- **Unit/thing management**: Interacts with `Thing` and `Object` hierarchies for rider handling.

## Design Patterns
- **Template Method**: `isSpecificRiderFreeToExit()` and `killRidersWhoAreNotFreeToExit()` allow subclasses to customize exit behavior.
- **Strategy**: Exit door reservation (`reserveDoorForExit`) decouples exit logic from transport implementation.
- **Observer**: `onContaining`/`onRemoving` notifies transport when riders join/leave (event-driven design).
