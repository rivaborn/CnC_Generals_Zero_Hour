# Generals/Code/Libraries/Source/WWVegas/WWMath/matrix3.cpp

## Purpose
Implements 3x3 matrix operations for 3D transformations, including multiplication, conversion from other matrix types, and orthogonalization.

## Responsibilities
- Provides matrix multiplication operators for Matrix3 and related types (Matrix3D, Matrix4)
- Supports conversion between Matrix3 and other matrix/quaternion types
- Implements orthogonalization checks and corrections
- Contains pre-defined rotation matrices (90Â°, 180Â°, 270Â° around X, Y, Z axes)

## Key Types
- Matrix3 (Class): 3x3 transformation matrix with row-major storage
- Matrix3D (External): 3x3 matrix type (used for compatibility)
- Matrix4 (External): 4x4 matrix type (used for compatibility)
- Quaternion (External): Quaternions for rotation representation

## Key Functions
### operator* (Matrix3D &, Matrix3 &)
- Purpose: Multiplies a Matrix3D with a Matrix3
- Calls: None (direct computation)

### operator* (Matrix3 &, Matrix3D &)
- Purpose: Multiplies a Matrix3 with a Matrix3D
- Calls: None (direct computation)

### Multiply (Matrix3 &, Matrix3 &, Matrix3 *)
- Purpose: Multiplies two Matrix3 instances with result storage control
- Calls: None (direct computation)

### Is_Orthogonal
- Purpose: Checks if the matrix is orthogonal (rows are unit vectors and orthogonal to each other)
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Re_Orthogonalize
- Purpose: Re-orthogonalizes the matrix by Gram-Schmidt process
- Calls: Vector3::Cross_Product, Vector3::Length, Make_Identity

## Globals
- Identity (Matrix3): Identity matrix (1s on diagonal)
- RotateX90/RotateX180/RotateX270 (Matrix3): Pre-defined X-axis rotation matrices
- RotateY90/RotateY180/RotateY270 (Matrix3): Pre-defined Y-axis rotation matrices
- RotateZ90/RotateZ180/RotateZ270 (Matrix3): Pre-defined Z-axis rotation matrices

## Dependencies
- matrix3.h (header for Matrix3 class)
- matrix3d.h (Matrix3D type)
- matrix4.h (Matrix4 type)
- quat.h (Quaternion type)
- Vector3 operations (external)
- WWMath::Fabs (external)
- WWMATH_EPSILON (external constant)
