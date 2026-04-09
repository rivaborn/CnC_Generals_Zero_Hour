# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/matrix3d.h

## Purpose
Defines the Matrix3D class and related math types for 3D transformations in the SAGE engine.

## Responsibilities
- Provides 4x4 homogeneous matrix operations (3x4 stored)
- Supports translation, rotation, scaling, and matrix inversion
- Implements vector-matrix multiplication and matrix-matrix multiplication
- Handles camera transformations (Look_At, Obj_Look_At)
- Optimized for right-handed coordinate systems and column-vectors

## Key Types
- Matrix3D (Class): 3D transformation matrix (4x4 homogeneous, stored as 3x4)
- Matrix3x3 (Class): 3x3 rotation matrix
- Matrix4x4 (Class): 4x4 matrix
- Quaternion (Class): Quaternion for rotations
- DynamicMatrix3D (Class): W3DMPO wrapper for Matrix3D

## Key Functions
### Matrix3D::operator==
- Purpose: Compares two matrices for equality
- Calls: None

### Matrix3D::operator!=
- Purpose: Compares two matrices for inequality
- Calls: operator==

### Matrix3D::submul
- Purpose: Helper for matrix multiplication without temporaries
- Calls: None

### Matrix3D::preMul
- Purpose: Pre-multiplies matrix (this = that * this)
- Calls: mul

### Matrix3D::postMul
- Purpose: Post-multiplies matrix (this = this * that)
- Calls: submul

### Matrix3D::mul
- Purpose: General matrix multiplication (this = A * B)
- Calls: submul

### Matrix3D::mulVector3
- Purpose: Transforms a 3D vector by the matrix
- Calls: None

### Matrix3D::Transform_Vector
- Purpose: Static vector transformation with alias handling
- Calls: None

### Matrix3D::Rotate_Vector
- Purpose: Static vector rotation with alias handling
- Calls: None

### Matrix3D::Inverse_Transform_Vector
- Purpose: Transforms vector by inverse matrix
- Calls: Inverse_Rotate_Vector

### Matrix3D::Inverse_Rotate_Vector
- Purpose: Rotates vector by inverse matrix
- Calls: None

## Globals
- Matrix3D::Identity (Matrix3D): Identity matrix
- Matrix3D::RotateX90 (Matrix3D): 90Â° rotation about X
- Matrix3D::RotateX180 (Matrix3D): 180Â° rotation about X
- Matrix3D::RotateX270 (Matrix3D): 270Â° rotation about X
- Matrix3D::RotateY90 (Matrix3D): 90Â° rotation about Y
- Matrix3D::RotateY180 (Matrix3D): 180Â° rotation about Y
- Matrix3D::RotateY270 (Matrix3D): 270Â° rotation about Y
- Matrix3D::RotateZ90 (Matrix3D): 90Â° rotation about Z
- Matrix3D::RotateZ180 (Matrix3D): 180Â° rotation about Z
- Matrix3D::RotateZ270 (Matrix3D): 270Â° rotation about Z

## Dependencies
- vector2.h, vector3.h, vector4.h
- always.h, assert.h
- W3DMPO (for DynamicMatrix3D)
- WWINLINE macro for inline functions
