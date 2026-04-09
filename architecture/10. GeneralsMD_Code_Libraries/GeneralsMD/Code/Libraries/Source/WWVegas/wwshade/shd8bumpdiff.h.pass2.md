# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpdiff.h - Enhanced Analysis

## Architectural Role
This file defines a shader class for bump-mapped diffuse lighting, integrating with the SAGE engine's rendering pipeline. It bridges the high-level shading interface (`ShdInterfaceClass`) with low-level hardware shaders (`ShdHWVertexShader`, `ShdHWPixelShader`), enabling advanced lighting effects while abstracting GPU-specific details.

## Cross-References
### Incoming
- Rendering pipeline (e.g., `ShdMeshClass`, `RenderInfoClass`) invokes `Pass_Selection`, `Apply_Shared`, and `Apply_Instance`.
- Vertex processing system calls `Copy_Vertex_Stream` for buffer management.

### Outgoing
- Relies on `ShdHWVertexShader` and `ShdHWPixelShader` for shader state setup.
- Uses `TextureClass` for diffuse/normal map binding.

## Design Patterns
- **Strategy Pattern**: `Shd8BumpDiffClass` implements `ShdInterfaceClass`, allowing dynamic selection of rendering techniques (e.g., self-shadowing).
- **Singleton-like Static Resources**: Vertex/pixel shaders and matrices are static, suggesting shared GPU state across instances.
- **Template Method**: `Apply_Shared`/`Apply_Instance` separate shared/per-instance state, enforcing a rendering pipeline structure.
