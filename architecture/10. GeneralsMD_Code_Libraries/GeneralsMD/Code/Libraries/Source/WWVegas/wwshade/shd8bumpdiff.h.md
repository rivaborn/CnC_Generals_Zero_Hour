# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpdiff.h

## Purpose
Defines the `Shd8BumpDiffClass` for handling bump-mapped diffuse shading in the SAGE engine.

## Responsibilities
- Manages bump-mapped diffuse rendering with normal maps
- Handles vertex/pixel shaders for hardware acceleration
- Supports self-shadowing effects
- Provides texture and vertex stream management

## Key Types
- **Shd8BumpDiffClass (Class)**: Bump-mapped diffuse shader implementation
- **ShdHWVertexShader (Static)**: Vertex shader for bump mapping
- **ShdHWPixelShader (Static)**: Pixel shader for bump mapping
- **Matrix4x4 (Static)**: View-projection matrix
- **TextureClass**: Diffuse and normal map textures

## Key Functions
### Shd8BumpDiffClass()
- Purpose: Constructor for bump-diffuse shader
- Calls: None

### Init()
- Purpose: Initializes static shader resources
- Calls: Not inferable

### Shutdown()
- Purpose: Releases static shader resources
- Calls: Not inferable

### Pass_Selection()
- Purpose: Determines which render pass to use
- Calls: Not inferable

### Apply_Shared()
- Purpose: Applies shared shader state for a pass
- Calls: Not inferable

### Apply_Instance()
- Purpose: Applies instance-specific shader state
- Calls: Not inferable

### Copy_Vertex_Stream()
- Purpose: Copies vertex data to a buffer
- Calls: Not inferable

### Setup_Self_Shadow_Info()
- Purpose: Configures self-shadowing parameters
- Calls: Not inferable

## Globals
- **Vertex_Shader (ShdHWVertexShader)**: Static vertex shader
