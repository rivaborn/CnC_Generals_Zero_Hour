# GeneralsMD/Code/GameEngine/Include/Common/DrawModule.h - Enhanced Analysis

## Architectural Role
This header defines the core rendering abstraction layer for the SAGE engine, serving as the bridge between game logic and the W3D rendering pipeline. It encapsulates drawable behavior for all in-game entities while providing performance estimation tools for the engine's rendering optimization systems.

## Cross-References
### Incoming
- Rendering subsystem (calls `doDrawModule`, `getRenderCost`)
- Game logic (calls `reactToTransformChange`, `reactToGeometryChange`)
- UI system (uses `isVisible` for occlusion culling)
- Network code (relies on `RenderCost` for bandwidth estimation)

### Outgoing
- W3D rendering backend (via abstract methods)
- Animation system (through `ObjectDrawInterface`)
- Particle system (via `updateBonesForClientParticleSystems`)
- Shadow rendering (through shadow-related methods)

## Design Patterns
- **Interface Segregation**: Multiple specialized interfaces (`ObjectDrawInterface`, `DebrisDrawInterface`) allow clients to depend only on relevant methods
- **Template Method**: `doDrawModule` defines rendering sequence while allowing subclasses to implement specific drawing logic
- **Composite**: `DrawModule` hierarchy enables uniform treatment of diverse drawable objects (units, effects, projectiles)
