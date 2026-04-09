# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpspec.h - Enhanced Analysis

## Architectural Role
This file defines the `Shd8BumpSpecClass`, a shader implementation for bump mapping and specular effects in the SAGE engine's rendering pipeline. It bridges the high-level shader interface (`ShdInterfaceClass`) with hardware-specific shader implementations (`ShdHWVertexShader`, `ShdHWPixelShader`), enabling advanced lighting effects for 3D models.

## Cross-References
### Incoming
- Rendering pipeline components (e.g., `ShdMeshClass`, `RenderInfoClass`) likely invoke `Pass_Selection`, `Apply_Shared`, and `Apply_Instance` during scene rendering.
- Vertex processing systems call `Copy_Vertex_Stream` for GPU buffer updates.

### Outgoing
- Relies on `ShdHWVertexShader` and `ShdHWPixelShader` for shader program management.
- Uses `TextureClass` for bump map and normal map resources.
- Interacts with `Matrix4x4` for view-projection transformations.

## Design Patterns
- **Strategy Pattern**: `Shd8BumpSpecClass` implements `ShdInterfaceClass` to provide a concrete shader strategy for bump/specular rendering.
- **Singleton-like Static Members**: Global shader objects (`Vertex_Shader`, `Pixel_Shader`) suggest shared resource management across instances.
- **Template Method**: `Apply_Shared`/`Apply_Instance` separation implies a two-phase rendering setup common in deferred shading pipelines.
