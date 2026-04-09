# Generals/Code/Libraries/Source/WWVegas/WWMath/matrix4.cpp

## Purpose
Implements matrix multiplication operations for 4x4 matrices and interactions with 3D matrices.

## Responsibilities
- Matrix4 Ã Matrix4 multiplication
- Matrix3D Ã Matrix4 multiplication
- Matrix4 Ã Matrix3D multiplication
- Result storage validation

## Key Types
- Matrix4 (class): 4x4 transformation matrix
- Matrix3D (class): 3D transformation matrix (external)

## Key Functions
### Matrix4::Multiply(const Matrix4 &a, const Matrix4 &b, Matrix4 *res)
- Purpose: Multiplies two 4x4 matrices.
- Calls: assert()

### Matrix4::Multiply(const Matrix3D &a, const Matrix4 &b, Matrix4 *res)
- Purpose: Multiplies a 3D matrix with a 4x4 matrix.
- Calls: assert()

### Matrix4::Multiply(const Matrix4 &a, const Matrix3D &b, Matrix4 *res)
- Purpose: Multiplies a 4x4 matrix with a 3D matrix.
- Calls: assert()

## Globals
None

## Dependencies
- matrix4.h (Matrix4, Matrix3D)
- assert.h (assert)
