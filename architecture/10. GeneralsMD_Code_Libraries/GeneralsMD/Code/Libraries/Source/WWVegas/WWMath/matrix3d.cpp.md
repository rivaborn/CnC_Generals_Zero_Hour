# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/matrix3d.cpp

## Purpose
Implements 3D matrix operations for the SAGE engine, including transformations, rotations, and matrix algebra.

## Responsibilities
- Provides 3D matrix arithmetic (multiplication, inversion)
- Handles matrix-vector transformations (rotation, translation)
- Supports matrix initialization from quaternions and 3x3 matrices
- Implements orthogonalization and matrix solving
- Contains optimized assembly implementations for key operations

## Key Types
- Matrix3D (class): 3x4 transformation matrix for 3D operations
- Matrix3x3 (external): 3x3 rotation matrix
- Quaternion (external): Quaternions for rotation
- Vector3 (external): 3D vector

## Key Functions
### Matrix3D::Multiply
- Purpose: Multiplies two 3D matrices
- Calls: None (inline assembly implementation)

### Matrix3D::Get_Inverse
- Purpose: Computes matrix inverse
- Calls: Matrix3D::Solve_Linear_System

### Matrix3D::Solve_Linear_System
- Purpose: Solves 3x3 linear system using Gauss-Jordan elimination
- Calls: None

### Matrix3D::Lerp
- Purpose: Linearly interpolates between two matrices
- Calls: Vector3::Lerp, Quaternion::Slerp

### Matrix3D::Re_Orthogonalize
- Purpose: Orthogonalizes matrix using Gram-Schmidt process
- Calls: Vector3::Cross_Product

## Globals
- Matrix3D::Identity (Matrix3D): Identity matrix
- Matrix3D::RotateX90/180/270 (Matrix3D): Predefined X-axis rotation matrices
- Matrix3D::RotateY90/180/270 (Matrix3D): Predefined Y-axis rotation matrices
- Matrix3D::RotateZ90/180/270 (Matrix3D): Predefined Z-axis rotation matrices

## Dependencies
- vector3.h, matrix3.h, matrix4.h, quat.h
- D3dx8math.h (DirectX math)
- WWMath namespace functions (Atan2, Sqrt, Fabs)
- Vector3 class methods (Dot_Product, Cross_Product, Lerp)
- Quaternion class methods (Slerp)
