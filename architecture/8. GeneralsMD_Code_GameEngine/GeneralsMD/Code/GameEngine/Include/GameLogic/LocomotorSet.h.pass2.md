# GeneralsMD/Code/GameEngine/Include/GameLogic/LocomotorSet.h - Enhanced Analysis

## Architectural Role
This file defines the `LocomotorSet` class, which is part of the game's movement system. It manages collections of `Locomotor` objects that define how entities move across different surface types (ground, water, cliffs, etc.). The class is critical for pathfinding and unit behavior, as it determines valid movement surfaces and handles serialization for save games.

## Cross-References
### Incoming
- **Unit/Entity Systems**: Likely called by unit classes to determine movement capabilities.
- **Pathfinding**: Used by the pathfinding subsystem to evaluate valid movement surfaces.
- **Save/Load**: Invoked during game serialization to preserve movement states.

### Outgoing
- **Locomotor**: Uses `Locomotor` objects to define movement behaviors.
- **LocomotorTemplate**: Relies on templates to instantiate locomotors.
- **Snapshot/Xfer**: Uses `Snapshot` and `Xfer` for serialization.

## Design Patterns
- **Composite**: `LocomotorSet` manages a collection of `Locomotor` objects, treating them as a single unit for movement logic.
- **Strategy**: Different `Locomotor` implementations can be swapped based on surface type, encapsulating movement behavior.
- **Singleton-like Usage**: While not a singleton, `LocomotorSet` is likely tightly coupled with unit instances, implying a per-unit movement strategy pattern.
