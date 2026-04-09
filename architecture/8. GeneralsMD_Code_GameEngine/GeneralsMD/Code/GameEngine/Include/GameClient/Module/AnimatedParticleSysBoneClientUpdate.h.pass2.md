# GeneralsMD/Code/GameEngine/Include/GameClient/Module/AnimatedParticleSysBoneClientUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a client-side update module for particle systems attached to animated bones, bridging the animation system with the particle system rendering pipeline. It extends the SAGE engine's modular architecture by implementing `ClientUpdateModule` to handle per-frame updates for bone-attached effects.

## Cross-References
### Incoming
- Likely called by the `Thing` class's update loop or the animation system's bone update mechanism
- Probably referenced in particle system initialization code (e.g., when attaching effects to bones)

### Outgoing
- Calls into the `Thing` class for bone position/transform data
- Uses `ClientUpdateModule` base class methods for module lifecycle management
- Interacts with particle system rendering components (not explicitly shown but implied)

## Design Patterns
- **Module Pattern**: Inherits from `ClientUpdateModule` to fit SAGE's pluggable architecture
- **Lifecycle Management**: Uses `m_life` counter for temporal behavior (likely for effect duration)
- **Memory Pool Pattern**: Uses SAGE's memory allocation system via `MEMORY_POOL_GLUE` macros
