# Generals/Code/Tools/WW3D/pluglib/matrix3d.h

## Purpose
Defines the Matrix3D class and related math operations for 3D transformations in the SAGE engine.

## Responsibilities
- Provides 4x4 homogeneous matrix operations (3x4 stored)
- Supports translation, rotation, and matrix multiplication
- Handles vector transformations and matrix interpolation
- Manages orthogonal matrix properties and inverses

## Key Types
- Matrix3D (Class): 3D transformation matrix with 3x4 storage (last row implicit)
- Matrix3 (Class): Forward declaration for 3x3 matrix
- Matrix4 (Class): Forward declaration for 4x4 matrix
- Quaternion (Class): Forward declaration for quaternion rotations

## Key Functions
### operator* (Matrix3D Ã Matrix3D)
- Purpose: Matrix multiplication
- Calls: None (inline implementation)

### operator* (Matrix3D Ã Vector3)
- Purpose: Transforms a vector by the matrix
- Calls: None (inline implementation)

### Lerp
- Purpose: Linearly interpolates between two matrices
- Calls: None (inline implementation)

### Matrix3D::Multiply
- Purpose: Static matrix multiplication with result parameter
- Calls: None (inline implementation)

### Matrix3D::Transform_Vector
- Purpose: Transforms a vector by a matrix with aliasing protection
- Calls: None (inline implementation)

## Globals
- Matrix3D::Identity (Matrix3D): Identity matrix constant
- Matrix3D::RotateX90/180/270 (Matrix3D): Predefined X-axis rotation matrices
- Matrix3D::RotateY90/180/270 (Matrix3D): Predefined Y-axis rotation matrices
- Matrix3D::RotateZ90/180/270 (Matrix3D): Predefined Z-axis rotation matrices

## Dependencies
- vector2.h, vector3.h, vector4.h: Vector math classes
- always.h: Common headers
- <assert.h>: Assertions
- osdep.h: Platform-specific definitions (Unix)
