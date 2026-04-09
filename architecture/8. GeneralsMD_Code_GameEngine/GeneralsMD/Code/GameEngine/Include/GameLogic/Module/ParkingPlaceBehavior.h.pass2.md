# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ParkingPlaceBehavior.h - Enhanced Analysis

## Architectural Role
This file defines the core parking management system for air units (helicopters/planes), bridging the gap between unit movement, production, and healing. It implements the `ParkingPlaceBehaviorInterface` and `ExitInterface`, acting as a mediator between units and structures like helipads or airfields.

## Cross-References
### Incoming
- **Unit Production System**: Calls `reserveSpace`/`releaseSpace` during unit creation/destruction.
- **AI Pathfinding**: Uses `getExitPosition`/`getNaturalRallyPoint` for navigation.
- **Damage System**: Invokes `onDie` when the parking structure is destroyed.

### Outgoing
- **Healing System**: Manages `HealingInfo` list and frame-based healing logic.
- **Door Management**: Interfaces with `ExitDoorType` for unit egress.
- **Team System**: Handles `defectAllParkedUnits` for team changes.

## Design Patterns
- **Strategy Pattern**: Implements `UpdateModule` and `DieModuleInterface` to encapsulate parking-specific behavior.
- **Resource Pooling**: Uses `std::vector<ParkingPlaceInfo>` to manage limited parking slots.
- **Observer Pattern**: Tracks healing progress via `HealingInfo` list with frame-based updates.
