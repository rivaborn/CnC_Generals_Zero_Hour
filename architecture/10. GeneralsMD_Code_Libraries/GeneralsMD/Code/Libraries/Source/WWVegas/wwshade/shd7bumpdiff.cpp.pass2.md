# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpdiff.cpp - Enhanced Analysis

## Architectural Role
This file implements a DirectX 7-compatible bump-mapping shader, bridging the engine's shader abstraction layer with low-level DX7 rendering. It handles vertex shader management, texture stage configuration, and lighting calculations for two-pass bump-diffuse rendering.

## Cross-References
### Incoming
- `ShdBumpDiffDefClass` (from shader definition system) - provides texture and material parameters
- `RenderInfoClass` - supplies lighting and camera data during rendering
- `WW3DAssetManager` - loads textures (diffuse and normal maps)

### Outgoing
- `DX8Wrapper` - for all DirectX state management and rendering calls
- `ShdHWVertexShader` - base class for vertex shader operations
- `ShdHWShader::Light` - inherited lighting calculation method

## Design Patterns
- **Strategy Pattern**: Vertex shader selection (hardware/software fallback) via `Is_Using_Hardware()`
- **Template Method**: `Apply_Shared`/`Apply_Instance` separation mirrors SAGE's shader pipeline architecture
- **Resource Management**: RAII for texture references via `REF_PTR_RELEASE` in destructor

*Not inferable*: Exact vertex shader code generation pipeline (preprocessed headers suggest external tooling).
