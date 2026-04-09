# Generals/Code/Libraries/Source/WWVegas/WWMath/matrix3d.cpp

## Purpose
Implements 3D matrix operations for the SAGE engine, including transformations, rotations, and linear algebra.

## Responsibilities
- Matrix initialization and manipulation
- 3D transformations (rotation, translation, scaling)
- Matrix inversion and orthogonality checks
- Linear interpolation and spherical interpolation
- Axis-aligned bounding box transformations

## Key Types
- Matrix3D (Class): 3x4 transformation matrix with rotation and translation
- Vector3 (Class): 3D vector operations
- Quaternion (Class): Quaternions for rotation
- Matrix3 (Class): 3x3 matrix operations
- Matrix4 (Class): 4x4 matrix operations

## Key Functions
### Matrix3D::Set
- Purpose: Initialize matrix from rotation and position
- Calls: None

### Matrix3D::Set_Rotation
- Purpose: Set rotation part of matrix from quaternion
- Calls: None

### Matrix3D::Get_X_Rotation
- Purpose: Approximate rotation about X axis
- Calls: WWMath::Atan2

### Matrix3D::Rotate_Vector
- Purpose: Rotate vector using 3x3 sub-matrix
- Calls: None

### Matrix3D::Look_At
- Purpose: Create "look at" transformation matrix
- Calls: WWMath::Sqrt

### Matrix3D::Transform_Min_Max_AABox
- Purpose: Compute transformed axis-aligned box
- Calls: None

### Matrix3D::Is_Orthogonal
- Purpose: Check if matrix is orthogonal
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Matrix3D::Re_Orthogonalize
- Purpose: Make matrix orthogonal
- Calls: Vector3::Cross_Product, Vector3::Length

### Matrix3D::Lerp
- Purpose: Linearly interpolate matrices
- Calls: Vector3::Lerp, Quaternion::Slerp

### Matrix3D::Solve_Linear_System
- Purpose: Solve 3x3 linear system using Gauss-Jordan elimination
- Calls: None

## Globals
- Matrix3D::Identity (Matrix3D): Identity matrix
- Matrix3D::RotateX90 (Matrix3D): 90-degree X rotation
- Matrix3D::RotateX180 (Matrix3D): 180-degree X rotation
- Matrix3D::RotateX270 (Matrix3D): 270-degree X rotation
- Matrix3D::RotateY90 (Matrix3D): 90-degree Y rotation
- Matrix3D::RotateY180 (Matrix3D): 180-degree Y rotation
- Matrix3D::RotateY270 (Matrix3D): 270-degree Y rotation
- Matrix3D::RotateZ90 (Matrix3D): 90-degree Z rotation
- Matrix3D::RotateZ180 (Matrix3D): 180-degree Z rotation
- Matrix3D::RotateZ270 (Matrix3D): 270-degree Z rotation

## Dependencies
- matrix3d.h
- vector3.h
- matrix3.h
- matrix4.h
- quat.h
- D3dx8math.h
- math.h
- assert.h
- stdlib.h
