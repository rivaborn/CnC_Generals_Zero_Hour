# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdcubemap.h - Enhanced Analysis

## Architectural Role
This file defines the cube map shader system within WWSHADE, bridging shader definitions (`ShdCubeMapDefClass`) with runtime implementation (`Shd6CubeMapClass`). It handles texture-based lighting effects, integrating with the broader rendering pipeline via `ShdInterfaceClass`.

## Cross-References
### Incoming
- **Rendering Pipeline**: Likely called by shader manager during material setup (e.g., `ShdInterfaceClass` consumers).
- **Asset System**: Used by level loaders or material editors for cube map definitions.

### Outgoing
- **WWSHADE Core**: Depends on `ShdDefClass`/`ShdInterfaceClass` for shader infrastructure.
- **D3D API**: Uses `D3DMATERIAL8` for fixed-function material states.
- **Math Library**: Relies on `Matrix4x4`/`Vector3`/`Vector4` for transformations and lighting.

## Design Patterns
- **Factory Pattern**: `ShdCubeMapDefClass::Create()` generates runtime shader instances.
- **Strategy Pattern**: `Apply_Shared`/`Apply_Instance` separate shared vs. per-instance state.
- **Composite**: Inherits from `ShdDefClass` to extend shader capabilities.
