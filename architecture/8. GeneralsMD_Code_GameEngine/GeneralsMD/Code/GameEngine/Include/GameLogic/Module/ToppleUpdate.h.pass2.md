# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ToppleUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core toppling physics module for objects in the game, bridging the game logic layer with the rendering and collision systems. It implements the state machine for toppling behavior and integrates with the FX system for visual feedback.

## Cross-References
### Incoming
- `StructureToppleUpdate.h` calls `applyTopplingForce` to initiate toppling on structures.
- Other behavior modules likely call `applyTopplingForce` to trigger toppling on dynamic objects.

### Outgoing
- Calls into `FXList` for visual effects during toppling/bouncing.
- Uses `UpdateModule` and `CollideModuleInterface` for game loop integration and collision handling.
- References `Thing` and `Object` for game entity interactions.

## Design Patterns
- **State Pattern**: Uses `ToppleState` enum to manage toppling phases (upright, falling, down).
- **Strategy Pattern**: Configurable options (`TOPPLE_OPTIONS_*`) allow runtime behavior modification.
- **Observer Pattern**: Implements `CollideModuleInterface` to react to collision events.

*Not inferable*: Exact physics calculations (e.g., angular velocity units) remain unclear without implementation details.
