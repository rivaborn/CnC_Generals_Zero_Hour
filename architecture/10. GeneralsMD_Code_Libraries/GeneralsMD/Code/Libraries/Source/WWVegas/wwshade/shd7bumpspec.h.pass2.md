# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpspec.h - Enhanced Analysis

## Architectural Role
This file defines the bump-mapping and specular shading implementation within the SAGE engine's rendering pipeline. It extends the `ShdInterfaceClass` to provide a two-pass shader solution for advanced lighting effects, integrating with the hardware shader system (`ShdHWVertexShader`) and texture management.

## Cross-References
### Incoming
- Rendering pipeline components (e.g., `RenderInfoClass`) call `Apply_Shared()` and `Apply_Instance()` during scene rendering.
- Vertex processing systems invoke `Copy_Vertex_Stream()` for vertex data preparation.
- Shader manager likely calls `Init()`/`Shutdown()` during engine startup/shutdown.

### Outgoing
- Relies on `ShdHWVertexShader` for vertex shader management (static instances `Pass_0_Vertex_Shader`/`Pass_1_Vertex_Shader`).
- Uses `TextureClass` for texture access (`Texture`/`NormalMap`).
- Depends on `ShdDefClass` for shader definition data (passed to constructor).

## Design Patterns
- **Template Method**: `Apply_Shared()`/`Apply_Instance()` define hooks for pass-specific shader logic.
- **Resource Pooling**: Static `ShdHWVertexShader` instances suggest shared shader resources across rendering calls.
- **Strategy**: Encapsulates bump-spec shading as a pluggable strategy within the broader shader system.
