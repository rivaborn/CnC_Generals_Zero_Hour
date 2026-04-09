# GeneralsMD/Code/GameEngine/Include/GameLogic/Locomotor.h - Enhanced Analysis

## Architectural Role
This file defines the core movement system for game entities, bridging physics simulation and game logic. It implements movement templates, physics interactions, and state management for units, serving as the runtime controller for all in-game movement behaviors.

## Cross-References
### Incoming
- Physics system calls `handleBehaviorZ` for vertical positioning
- Game logic calls `locoUpdate_moveTowardsPosition` and `locoUpdate_maintainCurrentPosition` for movement control
- Object system uses `LocomotorStore` for template retrieval

### Outgoing
- Calls into `PhysicsBehavior` for physical movement calculations
- Uses `LocomotorSet` for surface type management
- References `Damage` system for movement-impacting damage states

## Design Patterns
- **Template Method Pattern**: Movement behaviors are implemented via appearance-specific methods (e.g., `moveTowardsPositionLegs`, `moveTowardsPositionWheels`)
- **State Pattern**: Movement states (braking, climbing) are managed via bit flags (`LocoFlag`)
- **Singleton Pattern**: `LocomotorStore` provides global access to movement templates

*Not inferable*: Exact implementation of physics integration or networking impact.
