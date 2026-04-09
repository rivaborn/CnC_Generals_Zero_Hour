# Generals/Code/Libraries/Source/WWVegas/WW3D2/dazzle.cpp - Enhanced Analysis

## Architectural Role
This file implements the dazzle (light effects) subsystem, bridging rendering, configuration, and persistence. It handles dynamic light effects like halos and lens flares, integrating with the scene graph and camera systems.

## Cross-References
### Incoming
- **Rendering Pipeline**: Called by the main render loop to process visible dazzle effects
- **Scene Graph**: Uses `SceneClass` for visibility checks via `Compute_Point_Visibility`
- **Asset System**: Loads textures and shaders via `AssetMgrClass` and `ShaderClass`

### Outgoing
- **WW3D Core**: Uses `WW3D::Get_Frame_Time()` for timing
- **DX8 Wrapper**: DirectX state management via `DX8Wrapper::Set_Material`
- **Persistence**: Serializes dazzle objects via `ChunkLoadClass` and `PersistFactoryClass`

## Design Patterns
- **Factory Pattern**: `DazzlePrototypeClass` and `DazzleLoaderClass` create dazzle objects dynamically
- **Observer Pattern**: Dazzle objects register/unregister with `DazzleLayerClass` for visibility management
- **Strategy Pattern**: `DazzleVisibilityClass` provides pluggable visibility computation (default uses scene graph)

*Not inferable*: Exact shader management (e.g., whether using Render-to-Texture for lens flares).
