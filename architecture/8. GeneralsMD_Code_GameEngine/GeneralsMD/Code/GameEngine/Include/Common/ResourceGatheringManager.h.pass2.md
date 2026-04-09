# GeneralsMD/Code/GameEngine/Include/Common/ResourceGatheringManager.h - Enhanced Analysis

## Architectural Role
This file defines the `ResourceGatheringManager` class, which is part of the player's AI subsystem, specifically handling resource logistics. It bridges the gap between the economic layer (resource collection) and the tactical layer (unit movement decisions) by managing supply points and routing decisions for resource-gathering units.

## Cross-References
### Incoming
- **Player AI**: Likely called by the player's AI controller to make resource-gathering decisions.
- **Unit Logic**: Resource-gathering units (e.g., trucks) probably query this manager for optimal routes.
- **Building Logic**: Supply centers/warehouses may notify this manager upon creation/destruction.

### Outgoing
- **Object System**: Uses `ObjectID` to reference game entities, implying tight coupling with the core object management system.
- **Snapshot System**: Inherits from `Snapshot`, indicating integration with the game's save/load infrastructure.

## Design Patterns
- **Observer Pattern**: The manager tracks supply points dynamically, reacting to additions/removals (e.g., `addSupplyCenter`).
- **Strategy Pattern**: `findBestSupplyWarehouse`/`findBestSupplyCenter` encapsulate routing logic, allowing it to be modified without changing callers.
- **Memory Pool**: Uses `MemoryPoolObject` for optimized allocation, common in SAGE for performance-critical systems.
