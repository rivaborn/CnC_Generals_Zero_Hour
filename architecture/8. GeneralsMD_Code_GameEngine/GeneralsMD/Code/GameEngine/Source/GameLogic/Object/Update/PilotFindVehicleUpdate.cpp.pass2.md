# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/PilotFindVehicleUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the AI behavior for pilot units to autonomously find and board vehicles in need of repair. It integrates with the AI system, partition manager for spatial queries, and collision detection to determine valid targets.

## Cross-References
### Incoming
- AIUpdate.h (uses `AIUpdateInterface` for AI state management)
- CollideModule.h (queries `CollideModuleInterface` for collision compatibility)
- PartitionManager.h (uses `PartitionFilter` and `ObjectIterator` for spatial queries)

### Outgoing
- Calls into `UpdateModule` base class for serialization and update management
- Uses `PartitionManager` for object iteration and filtering
- Interacts with `AIUpdate` for AI state transitions (`aiEnter`, `aiMoveToPosition`)
- Queries `BodyModule` for health status checks

## Design Patterns
- **Strategy Pattern**: The `scanClosestTarget()` method encapsulates the target selection logic, allowing it to be modified independently.
- **Observer Pattern**: The update module reacts to AI state changes (`isIdle()`) to trigger scanning behavior.
- **Template Method**: The `update()` method follows a template for periodic AI behavior, with configurable sleep intervals.

Rules followed. Output under 400 tokens.
