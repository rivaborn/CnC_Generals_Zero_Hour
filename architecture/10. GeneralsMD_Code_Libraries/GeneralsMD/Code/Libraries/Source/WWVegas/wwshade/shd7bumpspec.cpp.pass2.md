# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpspec.cpp - Enhanced Analysis

## Architectural Role
This file implements the DirectX 7 bump specular shader, a legacy rendering feature in the SAGE engine. It bridges the fixed-function pipeline with early vertex shader capabilities, demonstrating the engine's support for both hardware and software rendering paths.

## Cross-References
### Incoming
- Rendering pipeline calls `Apply_Shared` and `Apply_Instance` during material setup
- Asset loading system references this via `ShdBumpSpecDefClass` initialization
- Vertex processing subsystem uses `Copy_Vertex_Stream` for mesh conversion

### Outgoing
- Directly manipulates DX8Wrapper for state management
- Uses WW3DAssetManager for texture loading
- Relies on ShdHWVertexShader for shader compilation

## Design Patterns
- **Strategy Pattern**: Different vertex shaders for each pass (Pass_0/1) can be swapped without changing client code
- **Facade Pattern**: Wraps complex DX8 state management behind simple method calls
- **Resource Pooling**: Static shader instances reused across multiple render calls

*Not inferable*: Exact relationship with software fallback path beyond the hardware check.
