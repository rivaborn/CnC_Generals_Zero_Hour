# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpspec.cpp - Enhanced Analysis

## Architectural Role
This file implements a DirectX 6-specific bump-specular shader, bridging the rendering pipeline and material system. It handles vertex shader setup, texture management, and per-instance render state configuration for gloss-mapped materials.

## Cross-References
### Incoming
- Rendering pipeline (via `Apply_Shared`/`Apply_Instance` calls)
- Material system (via `ShdDefClass` initialization)
- Asset manager (texture loading)

### Outgoing
- DX8Wrapper (render states, shader constants)
- Matrix4x4 (transform calculations)
- ShdHWVertexShader (lighting calculations)

## Design Patterns
- **Strategy Pattern**: Shader behavior varies based on hardware caps (e.g., `Support_ModAlphaAddClr()` check)
- **Singleton-like**: Static `Vertex_Shader` and `View_Projection_Matrix` suggest shared resource management
- **Template Method**: `Apply_Shared`/`Apply_Instance` separation mirrors SAGE's multi-pass rendering pattern

*Not inferable*: Exact vertex shader code flow (external `.vsh_code.h` file).
