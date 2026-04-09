# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpspec.cpp - Enhanced Analysis

## Architectural Role
This file implements the DirectX 8 bump-mapping and specular shading pipeline, serving as a critical component of the SAGE engine's rendering system. It bridges the shader definition system with hardware acceleration, managing both standard and self-shadowing rendering paths.

## Cross-References
### Incoming
- `ShdMeshClass` calls `Pass_Selection` and `Apply_Instance` during render passes
- `RenderInfoClass` is passed to `Apply_Shared` and `Setup_Self_Shadow_Info` for camera/view state
- `WW3DAssetManager` is queried for texture assets in constructor

### Outgoing
- Directly manipulates DX8Wrapper state (shaders, textures, matrices)
- Uses `Matrix4x4` for all transform calculations
- References shader code headers compiled from HLSL-like source

## Design Patterns
- **Singleton-like Shader Management**: Global shader objects (Vertex_Shader, Pixel_Shader) suggest a shared resource pattern
- **Strategy Pattern**: Different shader programs selected via `Pass_Selection` based on render context
- **Resource Wrapper**: `ShdHWVertexShader`/`ShdHWPixelShader` encapsulate DirectX shader objects

*Not inferable*: Exact factory pattern for shader creation, though `Create` methods suggest template-based instantiation.
