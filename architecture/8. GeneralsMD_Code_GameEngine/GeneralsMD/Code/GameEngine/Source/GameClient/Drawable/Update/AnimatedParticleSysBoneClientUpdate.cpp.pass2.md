# GeneralsMD/Code/GameEngine/Source/GameClient/Drawable/Update/AnimatedParticleSysBoneClientUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements a client-side update module for particle systems attached to skeletal bones, bridging the animation system and particle rendering. It operates in the client update pipeline, ensuring particle systems move with animated models without requiring server synchronization.

## Cross-References
### Incoming
- Called by the client update scheduler (not shown in file)
- Likely instantiated via `ThingFactory` for objects with bone-attached particles

### Outgoing
- Uses `Drawable` and `DrawModule` interfaces for bone updates
- Relies on `ClientUpdateModule` base class for core functionality
- Interacts with `ObjectDrawInterface` for bone transformations

## Design Patterns
- **Template Method**: Extends `ClientUpdateModule` with specialized `clientUpdate` logic
- **Visitor-like**: Iterates through draw modules to find bone-updating interfaces
- **State Counter**: Uses `m_life` as a simple timer for particle system control

*Not inferable*: Exact relationship with particle system lifecycle or animation event triggers.
