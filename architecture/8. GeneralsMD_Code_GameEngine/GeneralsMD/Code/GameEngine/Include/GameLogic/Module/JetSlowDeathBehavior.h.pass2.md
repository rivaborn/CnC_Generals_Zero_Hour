# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/JetSlowDeathBehavior.h - Enhanced Analysis

## Architectural Role
This file defines a specialized behavior module for jet aircraft death animations, extending the base `SlowDeathBehavior` to handle multi-stage destruction sequences with physics, visual effects, and audio. It integrates with the game's behavior system to provide realistic jet crash effects.

## Cross-References
### Incoming
- Likely called by `Thing` objects (units) when destroyed, particularly jet units
- Referenced in behavior module initialization code (e.g., `BehaviorModuleManager`)

### Outgoing
- Uses `SlowDeathBehavior` base class methods
- References `FXList` and `ObjectCreationList` for visual/audio effects
- Depends on `AudioEventRTS` for sound management

## Design Patterns
- **Template Method Pattern**: Extends `SlowDeathBehavior` with jet-specific death sequence logic
- **Data-Driven Design**: Uses `JetSlowDeathBehaviorModuleData` to configure behavior via external files (INI parsing)
- **Memory Pool Pattern**: Uses `MEMORY_POOL_GLUE` for object allocation optimization (common in SAGE engine)
