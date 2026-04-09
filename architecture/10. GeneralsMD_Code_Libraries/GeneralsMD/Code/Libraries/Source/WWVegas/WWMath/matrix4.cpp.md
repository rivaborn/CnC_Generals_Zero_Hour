# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/matrix4.cpp

## Purpose
Implements matrix multiplication operations for 4x4 matrices and comparison operators.

## Responsibilities
- Matrix4x4 multiplication (Matrix4x4 Ã Matrix4x4)
- Matrix4x4 multiplication (Matrix3D Ã Matrix4x4)
- Matrix4x4 multiplication (Matrix4x4 Ã Matrix3D)
- Matrix4x4 equality/inequality comparison

## Key Types
- Matrix4x4 (Class): 4x4 transformation matrix
- Matrix3D (Class): 3D transformation matrix (external)

## Key Functions
### Matrix4x4::Multiply (Matrix4x4 Ã Matrix4x4)
- Purpose: Multiplies two 4x4 matrices
- Calls: None

### Matrix4x4::Multiply (Matrix3D Ã Matrix4x4)
- Purpose: Multiplies a 3D matrix with a 4x4 matrix
- Calls: None

### Matrix4x4::Multiply (Matrix4x4 Ã Matrix3D)
- Purpose: Multiplies a 4x4 matrix with a 3D matrix
- Calls: None

### operator==
- Purpose: Compares two Matrix4x4 objects for equality
- Calls: None

### operator!=
- Purpose: Compares two Matrix4x4 objects for inequality
- Calls: operator==

## Globals
- None

## Dependencies
- matrix4.h (Matrix4x4, Matrix3D)
- assert.h (assert)
