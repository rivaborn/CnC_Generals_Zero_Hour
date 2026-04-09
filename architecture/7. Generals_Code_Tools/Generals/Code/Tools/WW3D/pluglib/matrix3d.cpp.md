# Generals/Code/Tools/WW3D/pluglib/matrix3d.cpp

## Purpose
Implements 3D transformation matrix operations for the W3D engine, including rotation, translation, and interpolation.

## Responsibilities
- Matrix construction and manipulation (rotation, translation, look-at)
- Matrix inversion and orthogonality checks
- Vector transformation and bounding box calculations
- Matrix interpolation (Lerp/Slerp)

## Key Types
- Matrix3D (Class): 3x4 transformation matrix with rotation/translation operations
- Quaternion (External): Used for rotation interpolation
- Vector3 (External): 3D vector for transformations

## Key Functions
### Lerp
- Purpose: Linearly interpolates between two matrices (position lerped, orientation slerped)
- Calls: Lerp (Vector3), Slerp (Quaternion), Build_Quaternion (Matrix3D), Matrix3D constructor

### Matrix3D::Get_Inverse
- Purpose: Computes matrix inverse (delegates to orthogonal inverse)
- Calls: Get_Orthogonal_Inverse

### Matrix3D::Get_Orthogonal_Inverse
- Purpose: Computes inverse for orthogonal matrices (transpose rotation, negate translated rotation)
- Calls: Get_Translation, Rotate_Vector

### Matrix3D::Transform_Min_Max_AABox
- Purpose: Transforms axis-aligned bounding box min/max corners
- Calls: None (uses direct matrix access)

### Matrix3D::Is_Orthogonal
- Purpose: Checks if matrix is orthogonal (orthonormal rows, zero dot products)
- Calls: Vector3::Dot_Product, WWMath::Fabs

## Globals
- Matrix3D::Identity (const Matrix3D): Identity matrix
- Matrix3D::RotateX90/180/270 (const Matrix3D): Predefined X-axis rotation matrices
- Matrix3D::RotateY90/180/270 (const Matrix3D): Predefined Y-axis rotation matrices
- Matrix3D::RotateZ90/180/270 (const Matrix3D): Predefined Z-axis rotation matrices

## Dependencies
- matrix3d.h (header)
- vector3.h (Vector3, WWMath)
- wwmatrix3.h (Matrix3)
- matrix4.h
- w3dquat.h (Quaternion)
- math.h, assert.h, stdlib.h
