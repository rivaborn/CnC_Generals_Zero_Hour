# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dazzle.cpp - Enhanced Analysis

## Architectural Role
This file implements the dazzle/lens flare rendering subsystem in WW3D, handling both the visual effects pipeline and persistence infrastructure. It bridges the rendering layer (DX8Wrapper) with scene management (SceneClass) and asset loading (INI parsing).

## Cross-References
### Incoming
- **Rendering Pipeline**: Called by the main render loop (likely in `scene.cpp` or `ww3d.cpp`) to render dazzle effects
- **Asset Loading**: Used by the W3D loader system (via `DazzleLoaderClass`) during level/map loading
- **Persistence System**: Referenced by save/load code (via `DazzlePersistFactoryClass`)

### Outgoing
- **Rendering Backend**: Uses `DX8Wrapper` for shader state management and `DX8VertexBuffer`/`DX8IndexBuffer` for geometry
- **Scene System**: Queries `SceneClass` for visibility calculations via `Compute_Point_Visibility`
- **Asset Management**: Loads textures via `AssetMgrClass` and INI parsing infrastructure

## Design Patterns
- **Factory Pattern**: `DazzlePersistFactoryClass` handles creation of dazzle objects during load
- **Strategy Pattern**: `DazzleVisibilityClass` provides pluggable visibility calculation (default uses scene occlusion)
- **Observer Pattern**: Dazzle objects register/unregister with `DazzleLayerClass` for visibility management

*Not inferable*: Exact shader management pattern (likely resource pooling given global shader objects).
