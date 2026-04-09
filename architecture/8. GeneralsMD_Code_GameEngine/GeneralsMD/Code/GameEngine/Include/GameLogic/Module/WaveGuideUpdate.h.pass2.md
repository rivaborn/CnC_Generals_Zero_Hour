# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WaveGuideUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the wave propagation system for water-based effects, bridging the physics simulation layer with visual/audio feedback. It extends the `UpdateModule` framework to handle dynamic water wave behavior, including damage application and environmental interactions.

## Cross-References
### Incoming
- **Physics System**: Likely calls `update()` during game loop to propagate waves
- **Audio System**: Uses `AudioEventRTS` for splash/looping sounds
- **Particle System**: References `ParticleSystemTemplate` for visual effects
- **Damage System**: Called by `doDamage()` to apply wave-related damage

### Outgoing
- **UpdateModule**: Inherits core update functionality
- **FieldParse**: Uses `buildFieldParse()` for configuration parsing
- **Thing System**: Interacts with game objects via `Thing*` parameter
- **Coord3D Math**: Uses 3D coordinates for wave shape calculations

## Design Patterns
- **Module Pattern**: Extends `UpdateModule` for composable game logic
- **Data-Driven Design**: Configuration via `WaveGuideUpdateModuleData` parsed from INI
- **Object Pooling**: Uses `MEMORY_POOL_GLUE` for performance optimization

*Not inferable*: Exact damage calculation or wave physics formulas.
