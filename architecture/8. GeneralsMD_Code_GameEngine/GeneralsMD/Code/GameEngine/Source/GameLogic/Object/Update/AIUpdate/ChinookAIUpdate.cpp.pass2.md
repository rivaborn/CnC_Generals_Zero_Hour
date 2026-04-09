# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/ChinookAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the specialized AI behavior for the Chinook helicopter unit, extending the base AIUpdate system with Chinook-specific states and mechanics. It bridges the gap between the generic AI framework and the unique transport/evacuation capabilities of the Chinook.

## Cross-References
### Incoming
- **AIUpdateInterface**: Calls `aiForceAttackObject`, `aiAttackPosition` for passenger units
- **ContainModuleInterface**: Uses `getContainedItemsList()`, `isPassengerAllowedToFire()`
- **UpgradeCenter**: Queries upgrade status for supply boost calculations

### Outgoing
- **ActionManager**: Likely used for command processing (implied by `privateForceAttackObject`)
- **PhysicsUpdate**: Manages takeoff/landing physics transitions
- **PartitionManager**: Used for spatial queries (implied by movement logic)

## Design Patterns
- **State Pattern**: Uses nested state machines (e.g., `ChinookTakeoffOrLandingState`) to manage complex flight behaviors
- **Visitor Pattern**: Implied by `Xfer` serialization methods in state classes
- **Composite Pattern**: Manages hierarchical relationships between Chinook and passengers via `ContainModuleInterface`

*Not inferable*: Exact command routing to passengers (truncated in source)
