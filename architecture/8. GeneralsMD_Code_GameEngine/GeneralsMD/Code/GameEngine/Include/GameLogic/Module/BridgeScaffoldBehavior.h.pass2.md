# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BridgeScaffoldBehavior.h - Enhanced Analysis

## Architectural Role
This file defines the behavior module for bridge scaffolds, a specialized game object used in bridge construction/teardown sequences. It bridges the gap between high-level bridge logic and low-level object motion, implementing state-driven animation for scaffold components.

## Cross-References
### Incoming
- Bridge construction/teardown logic (likely in `BridgeLogic` or similar)
- Object update system (via `UpdateModule` inheritance)
- Thing/Object management system

### Outgoing
- `Coord3D` for position calculations
- `BehaviorModule` and `UpdateModule` base classes
- Memory management system (via `MEMORY_POOL_GLUE`)

## Design Patterns
- **State Pattern**: Uses `ScaffoldTargetMotion` enum to represent different motion states, with `update()` dispatching to appropriate motion handlers
- **Interface/Implementation**: Separates abstract `BridgeScaffoldBehaviorInterface` from concrete implementation
- **Module Pattern**: Follows SAGE engine's component-based architecture with `UpdateModule` inheritance

*Not inferable*: Exact relationship with bridge construction sequence manager.
