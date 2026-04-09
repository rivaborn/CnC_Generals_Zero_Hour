# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/POWTruckAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the AI behavior for the POW Truck unit, integrating with the broader AI system (AIUpdate) and unit control framework. It implements a state machine for prisoner collection/transport, bridging between unit-specific logic and the game's command system.

## Cross-References
### Incoming
- `AIUpdate.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- Unit control systems (for command execution)

### Outgoing
- Prison/POW object systems (for target validation)
- Pathfinding/navigation (for movement logic)
- Command system (for player/ai command handling)

## Design Patterns
- **State Pattern**: Uses `POWTruckTask` enum to manage AI states (WAITING, FIND_TARGET, etc.), with separate update methods for each.
- **Strategy Pattern**: `validateTarget` and `findBestTarget` encapsulate selection logic, allowing for modular replacement.
- **Interface Segregation**: `POWTruckAIUpdateInterface` provides a minimal contract for external interaction, decoupling implementation from callers.
