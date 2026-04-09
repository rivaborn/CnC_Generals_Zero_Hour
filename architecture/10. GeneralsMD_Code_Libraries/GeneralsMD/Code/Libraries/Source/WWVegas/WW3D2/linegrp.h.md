# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/linegrp.h

## Purpose
Defines the `LineGroupClass` for rendering groups of lines, such as motion-blurred particle systems.

## Responsibilities
- Manages line rendering parameters (positions, colors, sizes, textures).
- Supports different line modes (tetrahedron, prism).
- Handles transformation flags and shader/texture application.
- Provides polygon count for rendering optimization.

## Key Types
- **LineGroupClass (Class)**: Main class for line group rendering.
- **FlagsType (Enum)**: Flags for transformation control.
- **LineModeType (Enum)**: Line rendering modes (TETRAHEDRON, PRISM).
- **RenderInfoClass (Class)**: External render info (forward declaration).
- **TextureClass (Class)**: External texture class (forward declaration).
- **ShareBufferClass<T> (Template Class)**: Shared buffer for vertex data.

## Key Functions
### `Set_Arrays`
- Purpose: Sets line vertex arrays (start/end positions, colors, sizes).
- Calls: None (direct).

### `Render`
- Purpose: Renders the line group using provided `RenderInfoClass`.
- Calls: None (direct).

### `Set_Line_Size`, `Get_Line_Size`
- Purpose: Sets/gets default line size.
- Calls: None.

### `Set_Texture`, `Get_Texture`, `Peek_Texture`
- Purpose: Manages texture assignment/retrieval.
- Calls: None.

### `Set_Shader`, `Get_Shader`
- Purpose: Sets/gets shader for line rendering.
- Calls: None.

## Globals
- None.

## Dependencies
- `shader.h`, `vector4.h`, `vector3.h`, `vector2.h` (includes).
- `RenderInfoClass`, `Texture
