# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matrixmapper.cpp

## Purpose
Implements texture coordinate mapping for 3D rendering, handling orthographic, perspective, and gradient projections.

## Responsibilities
- Manages view-to-texture and view-to-pixel transformations
- Applies texture mapping to Direct3D render states
- Supports composite texture mapping via nested mappers
- Computes texture coordinates for 3D points

## Key Types
- **MatrixMapperClass** (Class): Base texture mapper handling projection types
- **CompositeMatrixMapperClass** (Class): Wrapper for combining multiple texture mappers
- **Matrix4x4** (Struct): 4x4 transformation matrix (external)
- **Vector3** (Struct): 3D vector (external)

## Key Functions
### MatrixMapperClass::Update_View_To_Pixel_Transform
- Purpose: Recomputes view-to-pixel transformation matrix
- Calls: None

### MatrixMapperClass::Apply
- Purpose: Applies texture mapper to Direct3D render states
- Calls: DX8Wrapper::Set_Transform, DX8Wrapper::Set_DX8_Texture_Stage_State

### CompositeMatrixMapperClass::Apply
- Purpose: Applies composite texture mapping by combining internal mapper
- Calls: MatrixMapperClass::Apply, Matrix4x4::Multiply

### MatrixMapperClass::Calculate_Texture_Matrix
- Purpose: Calculates final texture matrix for external use
- Calls: None

## Globals
- None

## Dependencies
- **matrixmapper.h**: Header for MatrixMapperClass and related types
- **dx8wrapper.h**: Direct3D wrapper for render state management
- **Matrix4x4**, **Vector3**: Math types from external libraries
