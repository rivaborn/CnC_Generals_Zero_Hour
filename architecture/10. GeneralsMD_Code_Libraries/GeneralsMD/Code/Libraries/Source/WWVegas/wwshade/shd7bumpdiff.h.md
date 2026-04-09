# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpdiff.h

## Purpose
Defines the `Shd7BumpDiffClass` for bump-mapping and diffuse lighting in the SAGE engine.

## Responsibilities
- Manages bump-diffuse shader passes (2 passes)
- Handles vertex streams and hardware vertex processing
- Provides texture access (diffuse + normal map)
- Applies shared/instance-specific shader state

## Key Types
- **Shd7BumpDiffClass (Class)**: Bump-diffuse shader implementation.
- **ShdHWVertexShader (Static)**: Vertex shaders for each pass.
- **Matrix4x4 (Static)**: View-projection matrix.
- **TextureClass* (Members)**: Diffuse texture and normal map.

## Key Functions
### `Get_Pass_Count`
- Purpose: Returns the number of render passes (2).
- Calls: None.

### `Apply_Shared`
- Purpose: Applies shared shader state for a pass.
- Calls: Not inferable (implementation in .cpp).

### `Apply_Instance`
- Purpose: Applies instance-specific shader state for a pass.
- Calls: Not inferable (implementation in .cpp).

### `Copy_Vertex_Stream`
- Purpose: Copies vertex data for a stream.
- Calls: Not inferable (implementation in .cpp).

## Globals
- **Pass_0_Vertex_Shader (ShdHWVertexShader)**: Vertex shader for pass 0.
- **Pass_1_Vertex_Shader (ShdHWVertexShader)**: Vertex shader for pass 1.
- **View_Projection_Matrix (Matrix4x4)**: Shared view-projection matrix.

## Dependencies
- `shdinterface.h` (base class)
- `shdhwshader.h` (vertex sh
