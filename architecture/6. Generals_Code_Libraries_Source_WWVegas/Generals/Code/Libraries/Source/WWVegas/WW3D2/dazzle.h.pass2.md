# Generals/Code/Libraries/Source/WWVegas/WW3D2/dazzle.h - Enhanced Analysis

## Architectural Role
This header defines the core dazzle (light lens flare) system in the SAGE engine's rendering pipeline. It bridges the asset loading system (via `DazzleLoaderClass`) with the real-time rendering system, handling both static initialization and dynamic visibility/rendering of dazzle effects.

## Cross-References
### Incoming
- **Rendering System**: Calls `DazzleRenderObjClass::Render` during scene rendering
- **Asset System**: Uses `DazzleLoaderClass` to load dazzle prototypes from W3D files
- **Scene Management**: Relies on `DazzleLayerClass` for per-scene dazzle organization

### Outgoing
- **Shader System**: Uses `ShaderClass` for dazzle/halo shaders
- **Texture System**: References `TextureClass` for primary/secondary textures
- **Visibility System**: Integrates with `DazzleVisibilityClass` for occlusion testing

## Design Patterns
- **Prototype Pattern**: `DazzlePrototypeClass` enables runtime instantiation of dazzle effects from asset data
- **Strategy Pattern**: `DazzleVisibilityClass` allows pluggable visibility testing algorithms
- **Flyweight Pattern**: `DazzleTypeClass` centralizes shared dazzle parameters to reduce memory usage
