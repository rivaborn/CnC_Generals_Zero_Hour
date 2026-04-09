# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpspec.h

## Purpose
Defines the `Shd8BumpSpecClass` for handling 8-bit bump mapping and specular shading in the SAGE engine.

## Responsibilities
- Manages bump mapping and specular shading effects
- Handles vertex and pixel shaders for rendering
- Provides texture management for bump maps and normal maps
- Supports self-shadowing calculations
- Implements shader initialization and cleanup

## Key Types
- **Shd8BumpSpecClass (Class)**: Handles bump mapping and specular shading rendering

## Key Functions
### Shd8BumpSpecClass::Pass_Selection
- Purpose: Determines which rendering pass to use
- Calls: Not inferable

### Shd8BumpSpecClass::Apply_Shared
- Purpose: Applies shared shader state for rendering
- Calls: Not inferable

### Shd8BumpSpecClass::Apply_Instance
- Purpose: Applies instance-specific shader state for rendering
- Calls: Not inferable

### Shd8BumpSpecClass::Copy_Vertex_Stream
- Purpose: Copies vertex stream data for rendering
- Calls: Not inferable

### Shd8BumpSpecClass::Setup_Self_Shadow_Info
- Purpose: Sets up self-shadowing information for the mesh
- Calls: Not inferable

## Globals
- **Vertex_Shader (ShdHWVertexShader)**: Static vertex shader for bump mapping
- **Pixel_Shader (ShdHWPixelShader)**: Static pixel shader for bump mapping
- **View_Projection_Matrix (Matrix4x4)**: Static view-projection matrix
- **Self_Shadow_Pixel_Shader (ShdHWPixelShader)**: Static pixel shader for self-shadowing
-
