# Generals/Code/Libraries/Source/WWVegas/WWMath/matrix3d.h

## Purpose
Defines 3D transformation matrix classes and operations for the SAGE engine.

## Responsibilities
- Provides 3D matrix (Matrix3D) and dynamic matrix (DynamicMatrix3D) classes
- Implements matrix operations (multiplication, inversion, transformations)
- Supports vector transformations and matrix concatenation
- Handles orthogonal matrix operations and optimizations
- Manages matrix equality comparisons

## Key Types
- Matrix3D (Class): 3D transformation matrix with 12 floats (3x4, last row implicit)
- DynamicMatrix3D (Class): W3DMPO-derived wrapper for Matrix3D
- Matrix3 (Class): 3x3 matrix (forward declared)
- Matrix4 (Class): 4x4 matrix (forward declared)
- Quaternion (Class): Quaternion (forward declared)

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

## Globals
- Matrix3D::Identity (Matrix3D): Identity matrix
- Matrix3D::RotateX90 (Matrix3D): 90Â° X rotation matrix
- Matrix3D::RotateX180 (Matrix3D): 180Â° X rotation matrix
- Matrix3D::RotateX270 (Matrix3D): 270Â° X rotation matrix
- Matrix3D::RotateY90 (Matrix3D): 90Â° Y rotation matrix
- Matrix3D::RotateY180 (Matrix3D): 180Â° Y rotation matrix
- Matrix3D::RotateY270 (Matrix3D): 270Â° Y rotation matrix
- Matrix3D::RotateZ90 (Matrix3D): 90Â° Z rotation matrix
- Matrix3D::RotateZ180 (Matrix3D): 180Â° Z rotation matrix
- Matrix3D::RotateZ270 (Matrix3D): 270Â° Z rotation matrix

## Dependencies
- vector2.h, vector3.h, vector4.h
- always.h, assert.h
- W3DMPO (for DynamicMatrix3D)
- Matrix3, Matrix4, Quaternion (forward declared)
