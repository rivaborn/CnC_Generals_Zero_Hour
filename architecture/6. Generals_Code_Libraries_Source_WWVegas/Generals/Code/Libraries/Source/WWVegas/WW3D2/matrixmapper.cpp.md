# Generals/Code/Libraries/Source/WWVegas/WW3D2/matrixmapper.cpp

## Purpose
Implements texture coordinate transformation for rendering in the SAGE engine, handling view-to-texture and view-to-pixel matrix operations.

## Responsibilities
- Manages texture coordinate transformations for rendering stages
- Computes texture coordinates from 3D points
- Updates transformation matrices based on texture size and flags
- Applies transformations to DirectX texture stages

## Key Types
- **MatrixMapperClass (Class)**: Handles texture coordinate transformations for rendering
- **Matrix3D (Type)**: 3D transformation matrix
- **Matrix4 (Type)**: 4x4 transformation matrix
- **Vector3 (Type)**: 3D vector
- **D3DTRANSFORMSTATETYPE (Type)**: DirectX transform state type

## Key Functions
### MatrixMapperClass::MatrixMapperClass
- Purpose: Constructor initializing member variables
- Calls: None

### MatrixMapperClass::Set_Texture_Transform
- Purpose: Sets the viewspace-to-texturespace transform matrix
- Calls: Update_View_To_Pixel_Transform

### MatrixMapperClass::Update_View_To_Pixel_Transform
- Purpose: Recomputes the ViewToPixel transformation matrix
- Calls: None

### MatrixMapperClass::Compute_Texture_Coordinate
- Purpose: Computes a single texture coordinate from a 3D point
- Calls: None

### MatrixMapperClass::Apply
- Purpose: Applies the transformation to a DirectX texture stage
- Calls: DX8Wrapper::Set_Transform, DX8Wrapper::Set_DX8_Texture_Stage_State

## Globals
- None

## Dependencies
- matrixmapper.h
- dx8wrapper.h
- DirectX 8 types (D3DTRANSFORMSTATETYPE, D3DTSS_TEXCOORDINDEX, etc.)
