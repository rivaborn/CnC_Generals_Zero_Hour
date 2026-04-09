# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DScene.cpp - Enhanced Analysis

## Architectural Role
This file implements the core scene management system for the W3D rendering pipeline, acting as the bridge between game logic objects and the low-level rendering API (WW3D2). It handles visibility determination, occlusion culling, and special effect rendering, making it a critical component in the rendering hierarchy.

## Cross-References
### Incoming
- **GameClient/Drawable.h**: Uses DrawableInfo for visibility tracking
- **GameLogic/GameLogic.h**: Accesses frame count for occlusion timing
- **WW3D2/camera.h**: Uses camera for frustum culling
- **WW3D2/dx8renderer.h**: Interfaces with DirectX rendering pipeline

### Outgoing
- **GameClient/ParticleSys.h**: Calls DoParticles for particle effects
- **W3DDevice/GameClient/W3DShadow.h**: Manages shadow rendering
- **W3DDevice/GameClient/W3DShroud.h**: Handles shroud effects
- **WW3D2/Light.h**: Manages dynamic lighting

## Design Patterns
- **Observer Pattern**: Scene monitors game objects through DrawableInfo callbacks
- **Strategy Pattern**: Different rendering passes (shroud, heat vision) use interchangeable material passes
- **Flyweight Pattern**: Reuses global lights across multiple objects

*Not inferable*: Exact implementation of occlusion culling algorithm (ray casting vs. depth-based)
