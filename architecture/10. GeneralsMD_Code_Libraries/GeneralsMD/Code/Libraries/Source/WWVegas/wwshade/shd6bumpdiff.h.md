# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpdiff.h

## Purpose
Defines the `Shd6BumpDiffClass` for handling bump-mapped diffuse shading in the SAGE engine.

## Responsibilities
- Manages bump-mapped diffuse shading passes
- Provides texture and vertex stream access
- Handles hardware vertex processing
- Initializes/shuts down static shader resources

## Key Types
- **Shd6BumpDiffClass (Class)**: Bump-mapped diffuse shader implementation
- **ShdHWVertexShader (Static)**: Vertex shader for hardware processing
- **Matrix4x4 (Static)**: View-projection matrix
- **TextureClass* (Member)**: Diffuse texture reference
- **Vector4 (Members)**: Ambient/diffuse material colors

## Key Functions
### Shd6BumpDiffClass()
- Purpose: Constructor for bump-diffuse shader
- Calls: Not inferable

### Init()
- Purpose: Initializes static shader resources
- Calls: Not inferable

### Shutdown()
- Purpose: Cleans up static shader resources
- Calls: Not inferable

### Apply_Shared()
- Purpose: Applies shared shader state for rendering
- Calls: Not inferable

### Apply_Instance()
- Purpose: Applies per-instance shader state
- Calls: Not inferable

### Copy_Vertex_Stream()
- Purpose: Copies vertex data to destination buffer
- Calls: Not inferable

## Globals
- **Vertex_Shader (ShdHWVertexShader)**: Static vertex shader instance
- **View_Projection_Matrix (Matrix4x4)**: Static view-projection matrix

## Dependencies
- `shdinterface.h` (ShdInterfaceClass)
- `shdhwshader.h` (ShdHWVertexShader)
