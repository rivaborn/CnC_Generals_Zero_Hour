# GeneralsMD/Code/GameEngine/Include/Common/DamageFX.h - Enhanced Analysis

## Architectural Role
This file defines the core damage effect system, bridging game logic (damage application) and presentation (visual/audio effects). It serves as the central registry for damage reactions, allowing units to dynamically query appropriate effects based on damage type and severity.

## Cross-References
### Incoming
- **GameLogic/Module/Body.h**: Uses DamageFX for damage reaction effects
- **GameLogic/Module/TransitionDamageFX.h**: Extends damage effects with state transitions
- **W3D/ParticleSystem.h**: Likely referenced by FXList for particle-based effects

### Outgoing
- **INI parsing system**: For configuration loading
- **FXList system**: For effect sequencing
- **Object system**: For source/victim context in effects

## Design Patterns
- **Singleton Pattern**: DamageFXStore provides global access to damage effects
- **Strategy Pattern**: DamageFX encapsulates different damage reaction strategies per type
- **Flyweight Pattern**: DamageFX instances are shared across units to minimize memory usage

*Not inferable*: Exact relationship with W3D rendering system or audio subsystem.
