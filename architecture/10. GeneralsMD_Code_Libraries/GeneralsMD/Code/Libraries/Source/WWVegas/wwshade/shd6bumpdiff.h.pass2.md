# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpdiff.h - Enhanced Analysis

## Architectural Role
This file defines a specialized shader class (`Shd6BumpDiffClass`) for bump-mapped diffuse lighting, integrating into the SAGE engine's rendering pipeline. It extends the base shader interface (`ShdInterfaceClass`) and interacts with the hardware shader subsystem (`ShdHWVertexShader`), bridging high-level material properties with low-level GPU operations.

## Cross-References
### Incoming
- Rendering subsystem calls `Apply_Shared()` and `Apply_Instance()` during material setup
- Vertex processing code invokes `Copy_Vertex_Stream()` for buffer management
- Shader manager uses `Init()`/`Shutdown()` for resource lifecycle

### Outgoing
- Relies on `ShdHWVertexShader` for hardware acceleration
- Uses `TextureClass` for diffuse texture binding
- Depends on `ShdInterfaceClass` for shader pipeline integration

## Design Patterns
- **Template Method**: `Apply_Shared()`/`Apply_Instance()` define hooks for rendering pipeline
- **Singleton-like**: Static `Vertex_Shader` and `View_Projection_Matrix` suggest shared resource pattern
- **Strategy**: Encapsulates bump-diffuse algorithm as a replaceable shader strategy

*Not inferable*: Exact vertex shader implementation details or texture sampling behavior.
