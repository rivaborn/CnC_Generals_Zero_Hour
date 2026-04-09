# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DModelDraw.h - Enhanced Analysis

## Architectural Role
This header defines the core 3D model rendering interface for the SAGE engine, bridging the W3D rendering system with game-specific model behavior. It manages animation states, transitions, and visual effects while coordinating with particle systems, shadows, and weapon effects.

## Cross-References
### Incoming
- **GameClient/Module/** - Uses this for particle system integration
- **WW3D2/** - Depends on W3D rendering primitives
- **Common/** - Relies on model state and draw module abstractions

### Outgoing
- **GameClient/ParticleSys.h** - Manages particle system attachments
- **Common/ModelState.h** - Uses model condition state definitions
- **WW3D2/RendObj.h** - Interfaces with W3D render objects

## Design Patterns
- **State Pattern** - ModelConditionInfo manages different model states with transitions
- **Observer Pattern** - Particle systems track bone transformations
- **Strategy Pattern** - Different animation modes (loop, once, etc.) are selectable

*Not inferable: Exact implementation details of patterns without seeing usage context.*
