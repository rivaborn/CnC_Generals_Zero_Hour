# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/matrix3.cpp

## Purpose
Implements 3x3 matrix operations for the game's math library, including matrix multiplication, conversion from other matrix types, and orthogonalization.

## Responsibilities
- Provides matrix multiplication operators for Matrix3x3 with Matrix3D/Matrix4x4
- Implements matrix conversion constructors and assignment operators
- Contains utility functions for matrix operations (orthogonalization, identity checks)
- Defines pre-initialized rotation matrices (90Â°, 180Â°, 270Â° around X, Y, Z axes)
- Handles quaternion-to-matrix conversion

## Key Types
- Matrix3x3 (Class): 3x3 transformation matrix with row-major storage
- Vector3 (Class): Used for matrix elements and operations
- Quaternion (Class): Used for rotation matrix conversion

## Key Functions
### operator* (Matrix3D &, Matrix3x3 &)
- Purpose: Multiplies a Matrix3D with a Matrix3x3
- Calls: ROWCOL macro for element-wise multiplication

### operator* (Matrix3x3 &, Matrix3D &)
- Purpose: Multiplies a Matrix3x3 with a Matrix3D
- Calls: ROWCOL macro for element-wise multiplication

### Multiply (Matrix3x3 &, Matrix3x3 &, Matrix3x3 *)
- Purpose: Multiplies two Matrix3x3 objects with result storage option
- Calls: None (direct element-wise computation)

### Is_Orthogonal
- Purpose: Checks if matrix is orthogonal (rows are orthonormal vectors)
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Re_Orthogonalize
- Purpose: Orthogonalizes matrix using Gram-Schmidt process
- Calls: Vector3::Cross_Product, Vector3::Length, Make_Identity

## Globals
- Identity (Matrix3x3): Identity matrix (1s on diagonal)
- RotateX90/180/270 (Matrix3x3): Pre-initialized X-axis rotation matrices
- RotateY90/180/270 (Matrix3x3): Pre-initialized Y-axis rotation matrices
- RotateZ90/180/270 (Matrix3x3): Pre-initialized Z-axis rotation matrices

## Dependencies
- matrix3.h, matrix3d.h, matrix4.h, quat.h
- Vector3 class methods (Dot_Product, Cross_Product, Length)
- WWMath::Fabs
- WWMATH_EPSILON constant
