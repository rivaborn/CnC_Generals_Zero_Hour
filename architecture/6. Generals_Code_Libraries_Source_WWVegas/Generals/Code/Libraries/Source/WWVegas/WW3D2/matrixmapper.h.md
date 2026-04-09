# Generals/Code/Libraries/Source/WWVegas/WW3D2/matrixmapper.h

## Purpose
Defines the `MatrixMapperClass` for computing texture coordinates in projected textures within the SAGE engine.

## Responsibilities
- Manages texture coordinate computation for projected textures
- Handles different mapping types (ortho/perspective/depth/normal gradients)
- Maintains view-to-texture and view-to-pixel transformation matrices
- Provides gradient coordinate control for depth/normal mapping

## Key Types
- **MatrixMapperClass (Class)**: Texture coordinate mapper for projected textures
- **(anonymous enum) (Enum)**: Flag for depth gradient inversion
- **INVERT_DEPTH_GRADIENT (Enum)**: Flag to invert depth gradient
- **MappingType (Enum)**: Type of texture mapping (ortho/perspective/depth/normal)
- **ORTHO_PROJECTION (Enum)**: Orthographic projection type
- **PERSPECTIVE_PROJECTION (Enum)**: Perspective projection type
- **DEPTH_GRADIENT (Enum)**: Depth gradient mapping type
- **NORMAL_GRADIENT (Enum)**: Normal gradient mapping type

## Key Functions
### `MatrixMapperClass(int stage)`
- Purpose: Constructor for MatrixMapperClass
- Calls: None

### `Set_Flag(uint32 flag, bool onoff)`
- Purpose: Sets or clears a flag
- Calls: None

### `Get_Flag(uint32 flag) const`
- Purpose: Retrieves a flag state
- Calls: None

### `Set_Type(MappingType type)`
- Purpose: Sets the mapping type
- Calls: None

### `Get_Type()`
- Purpose: Retrieves the current mapping type
- Calls: None

### `Set_Texture_Transform(const Matrix3D &, float texsize)`
- Purpose: Sets the view
