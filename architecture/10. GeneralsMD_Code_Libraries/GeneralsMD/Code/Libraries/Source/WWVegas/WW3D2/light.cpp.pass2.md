# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/light.cpp - Enhanced Analysis

## Architectural Role
This file implements the core lighting system for the WW3D2 engine, bridging between the scene graph and the rendering pipeline. It handles light properties, serialization, and registration with the scene, serving as the central authority for all lighting operations in the engine.

## Cross-References
### Incoming
- Scene management (SceneClass) calls `Notify_Added`/`Notify_Removed` during scene graph operations
- W3D file loading/saving infrastructure uses `Load_W3D`/`Save_W3D` for asset serialization
- Persistence system calls `Save`/`Load` for game state serialization

### Outgoing
- Calls into `SceneClass` for light registration/unregistration
- Uses `ChunkSaveClass`/`ChunkLoadClass` for persistence
- Interfaces with `W3dUtilityClass` for color/vector conversion
- Depends on `RenderObjClass` for base functionality

## Design Patterns
- **Factory Pattern**: Uses `SimplePersistFactoryClass` for object creation and persistence
- **Observer Pattern**: Implements `Notify_Added`/`Notify_Removed` for scene graph integration
- **Composite Pattern**: LightClass inherits from `RenderObjClass`, fitting into the scene graph hierarchy

*Not inferable*: Specific implementation details of attenuation calculations or spot light behavior.
