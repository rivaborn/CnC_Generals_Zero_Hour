# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpspec.h

## Purpose
Defines the `Shd7BumpSpecClass` for handling bump-mapping and specular shading in the SAGE engine.

## Responsibilities
- Manages bump-mapping and specular shading passes
- Provides texture access and vertex stream handling
- Initializes and shuts down shader resources
- Applies shared and instance-specific shader states

## Key Types
- **Shd7BumpSpecClass (Class)**: Bump-mapping and specular shading implementation.

## Key Functions
### Shd7BumpSpecClass()
- Purpose: Constructor for bump-spec shader.
- Calls: Not inferable.

### Init()
- Purpose: Initializes static shader resources.
- Calls: Not inferable.

### Shutdown()
- Purpose: Releases static shader resources.
- Calls: Not inferable.

### Get_Pass_Count()
- Purpose: Returns the number of rendering passes (2).
- Calls: None.

### Apply_Shared()
- Purpose: Applies shared shader state for a pass.
- Calls: Not inferable.

### Apply_Instance()
- Purpose: Applies instance-specific shader state for a pass.
- Calls: Not inferable.

### Copy_Vertex_Stream()
- Purpose: Copies vertex stream data for rendering.
- Calls: Not inferable.

## Globals
- **Pass_0_Vertex_Shader (ShdHWVertexShader)**: Vertex shader for pass 0.
- **Pass_1_Vertex_Shader (ShdHWVertexShader)**: Vertex shader for pass 1.
- **View_Projection_Matrix (Matrix4x4)**: Combined view/projection matrix.
- **Texture (TextureClass*)**: Main texture.
- **NormalMap (TextureClass*)**: Normal map texture.
