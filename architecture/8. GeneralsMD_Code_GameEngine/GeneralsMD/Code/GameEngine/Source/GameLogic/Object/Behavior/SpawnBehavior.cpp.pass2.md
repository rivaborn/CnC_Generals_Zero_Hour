# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/SpawnBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the core spawning logic for units in the game, acting as a bridge between the spawner object and its spawned units. It manages the lifecycle of spawned units, including creation, health aggregation, and death propagation, while also handling selection and AI synchronization.

## Cross-References
### Incoming
- **GameLogic/Object/Behavior/BehaviorModule.cpp**: Inherits from `BehaviorModule`, likely called during behavior updates.
- **GameLogic/Module/AIUpdate.cpp**: Uses `aiForceAttackObject` to order slaves to attack.
- **GameClient/Drawable.cpp**: Syncs selection state via `isSelected` and `selectDrawable`.
- **GameLogic/ExperienceTracker.cpp**: Aggregates veterancy levels from spawned units.

### Outgoing
- **GameLogic/GameLogic.cpp**: Uses `findObjectByID` and `destroyObject` for spawned unit management.
- **Common/ThingFactory.cpp**: Retrieves templates via `findTemplate`.
- **GameLogic/Module/BodyModule.cpp**: Sets initial health on spawned units.
- **GameLogic/Module/StealthUpdate.cpp**: Checks stealth status of spawned units.

## Design Patterns
- **Observer Pattern**: SpawnBehavior monitors spawned units for death/health changes, reacting to state updates.
- **State Aggregation**: Combines health/veterancy/selection from multiple spawned units into the spawner's state.
- **Template Method**: Uses `ThingTemplate` for unit creation, allowing dynamic spawning without hardcoding unit types.
