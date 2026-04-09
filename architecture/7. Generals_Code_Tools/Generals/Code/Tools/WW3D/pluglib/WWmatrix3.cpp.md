# Generals/Code/Tools/WW3D/pluglib/WWmatrix3.cpp

## Purpose
Implements the Matrix3 class for 3D matrix operations, including multiplication, conversion from other matrix types, and utility functions.

## Responsibilities
- Provides matrix multiplication operators and methods
- Handles conversions between Matrix3, Matrix3D, Matrix4, and Quaternion
- Implements matrix utility functions (orthogonality checks, re-orthogonalization)
- Manages pre-initialized common rotation matrices
- Supports axis-aligned bounding box rotation

## Key Types
- Matrix3 (Class): 3x3 transformation matrix with row-major storage
- Matrix3D (External): 3x3 matrix type (used for compatibility)
- Matrix4 (External): 4x4 matrix type (used for compatibility)
- Quaternion (External): Quaternions for rotation representation
- Vector3 (External): 3D vector type

## Key Functions
### operator* (Matrix3D &, Matrix3 &)
- Purpose: Multiplies a Matrix3D with a Matrix3
- Calls: None (direct computation)

### operator* (Matrix3 &, Matrix3D &)
- Purpose: Multiplies a Matrix3 with a Matrix3D
- Calls: None (direct computation)

### Matrix3::Multiply
- Purpose: Performs matrix multiplication with various input combinations
- Calls: None (direct computation)

### Matrix3::Set
- Purpose: Sets matrix values from Matrix3D or Matrix4
- Calls: Vector3::Set

### Matrix3::Re_Orthogonalize
- Purpose: Ensures matrix remains orthogonal by recomputing basis vectors
- Calls: Vector3::Cross_Product, Vector3::Length, Vector3::operator/

## Globals
- Matrix3::Identity (Matrix3): Identity matrix (1,0,0; 0,1,0; 0,0,1)
- Matrix3::RotateX90/180/270 (Matrix3): Pre-initialized X-axis rotation matrices
- Matrix3::RotateY90/180/270 (Matrix3): Pre-initialized Y-axis rotation matrices
- Matrix3::RotateZ90/180/270 (Matrix3): Pre-initialized Z-axis rotation matrices

## Dependencies
- wwmatrix3.h (header)
- matrix3d.h (Matrix3D)
- matrix4.h (Matrix4)
- w3dquat.h (Quaternion)
- Vector3 operations (external)
