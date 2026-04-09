# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpspec.h

## Purpose
Defines the `Shd6BumpSpecClass` for handling bump-mapping and specular shading in the SAGE engine.

## Responsibilities
- Manages bump-mapping and specular shading effects
- Provides texture and vertex stream access for rendering
- Handles hardware vertex processing
- Initializes and shuts down shader resources

## Key Types
- **Shd6BumpSpecClass (Class)**: Bump-mapping and specular shading implementation

## Key Functions
### Shd6BumpSpecClass()
- Purpose: Constructor for bump-spec shader.
- Calls: None

### ~Shd6BumpSpecClass()
- Purpose: Destructor for bump-spec shader.
- Calls: None

### Init()
- Purpose: Initializes static shader resources.
- Calls: None

### Shutdown()
- Purpose: Releases static shader resources.
- Calls: None

### Get_Pass_Count()
- Purpose: Returns the number of rendering passes (always 1).
- Calls: None

### Get_Texture_Count()
- Purpose: Returns the number of textures used (always 1).
- Calls: None

### Peek_Texture()
- Purpose: Returns the bump-spec texture.
- Calls: None

### Apply_Shared()
- Purpose: Applies shared shader state for rendering.
- Calls: None

### Apply_Instance()
- Purpose: Applies instance-specific shader state for rendering.
- Calls: None

### Get_Vertex_Stream_Count()
- Purpose: Returns the number of vertex streams.
- Calls: None

### Get_Vertex_Size()
- Purpose: Returns the size of a vertex stream.
- Calls: None

### Use_HW_Vertex_Processing()
- Purpose
