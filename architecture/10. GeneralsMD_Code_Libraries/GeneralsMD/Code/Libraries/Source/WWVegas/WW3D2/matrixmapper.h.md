# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matrixmapper.h

## Purpose
Defines classes for texture coordinate mapping in the 3D rendering pipeline, supporting projected textures and composite mappings.

## Responsibilities
- Manages texture coordinate computation for projected textures
- Handles view-to-texture and view-to-pixel transformations
- Supports different mapping types (ortho/perspective/depth/normal gradients)
- Provides composite mapping functionality via internal mapper

## Key Types
- **MatrixMapperClass (Class)**: Base class for texture coordinate mapping with projection support
- **CompositeMatrixMapperClass (Class)**: Extends MatrixMapperClass to composite with an internal mapper
- **MappingType (Enum)**: Defines projection types (ORTHO_PROJECTION, PERSPECTIVE_PROJECTION, DEPTH_GRADIENT, NORMAL_GRADIENT)
- **INVERT_DEPTH_GRADIENT (Enum)**: Flag for depth gradient inversion

## Key Functions
### MatrixMapperClass::Apply
- Purpose: Applies the texture mapping transformation
- Calls: Calculate_Texture_Matrix, Update_View_To_Pixel_Transform

### MatrixMapperClass::Calculate_Texture_Matrix
- Purpose: Computes the final texture matrix
- Calls: Not inferable

### CompositeMatrixMapperClass::Apply
- Purpose: Applies composite mapping using internal mapper
- Calls: Calculate_Texture_Matrix

### CompositeMatrixMapperClass::Calculate_Texture_Matrix
- Purpose: Composites internal mapper's matrix with its own
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `bittype.h`, `matrix4.h`, `mapper.h`
- `TextureMapperClass`, `Matrix3D`, `Matrix4x4`, `Vector3`
