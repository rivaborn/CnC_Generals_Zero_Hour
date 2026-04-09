# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dazzle.h - Enhanced Analysis

## Architectural Role
This file defines the core dazzle (lighting/flare) effect system in the SAGE engine's rendering pipeline. It bridges the asset loading system (W3D prototypes) with runtime rendering, handling both static initialization and dynamic visibility calculations.

## Cross-References
### Incoming
- **Rendering System**: Calls `Render()` and `Special_Render()` during scene rendering
- **Asset System**: Uses `DazzleLoaderClass` for W3D chunk loading
- **Camera System**: Interacts with `CameraClass` for visibility calculations

### Outgoing
- **Shader System**: Uses `ShaderClass` for dazzle/halo effects
- **Texture System**: References `TextureClass` for primary/secondary textures
- **Visibility System**: Integrates with `DazzleVisibilityClass` for custom visibility tests

## Design Patterns
- **Prototype Pattern**: `DazzlePrototypeClass` enables runtime creation of dazzle objects from W3D assets
- **Strategy Pattern**: `DazzleVisibilityClass` allows pluggable visibility calculation strategies
- **Singleton Pattern**: Global `_DazzleLoader` instance manages asset loading (implicit)

*Not inferable*: Exact shader/rendering pipeline integration details.
