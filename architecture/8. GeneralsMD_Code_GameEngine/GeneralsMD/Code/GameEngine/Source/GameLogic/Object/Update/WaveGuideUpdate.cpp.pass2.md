# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/WaveGuideUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the water wave simulation system, bridging terrain modification, particle effects, and damage logic. It extends the `UpdateModule` base class to handle dynamic wave behavior, including path following, visual effects, and environmental interactions.

## Cross-References
### Incoming
- **AIUpdate.cpp**: Calls `startMoving` to initiate wave path following
- **PhysicsUpdate.cpp**: Likely references wave state during collision checks
- **TerrainLogic.cpp**: Uses wave damage results to update terrain state

### Outgoing
- **ParticleSystemManager**: Creates/destroys wave-related particle effects
- **TerrainLogic**: Queries waypoints and applies water damage
- **AudioSystem**: Triggers splash/looping sounds
- **PartitionManager**: Iterates objects for damage application

## Design Patterns
- **Strategy Pattern**: Wave behavior (damage, effects) is encapsulated in modular methods (`doDamage`, `doShapeEffects`)
- **Observer Pattern**: Listens to frame updates via `update()` to trigger periodic effects
- **State Pattern**: Implicit state management (initialized/active) controls wave lifecycle

*Not inferable*: No clear use of Visitor or Factory patterns despite object creation/destruction.
