# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/matrix4.h

## Purpose
Defines the Matrix4x4 class for 4x4 matrix operations, including construction, arithmetic, and transformations.

## Responsibilities
- Provides 4x4 matrix construction and initialization
- Implements matrix arithmetic (addition, subtraction, multiplication)
- Supports matrix-vector transformations
- Handles projection matrix initialization (orthographic/perspective)
- Offers matrix operations (transpose, inverse)

## Key Types
- Matrix4x4 (Class): 4x4 matrix representation with row-major storage

## Key Functions
### Matrix4x4::Make_Identity
- Purpose: Sets matrix to identity
- Calls: Vector4::Set

### Matrix4x4::Init_Ortho
- Purpose: Initializes orthographic projection matrix
- Calls: Make_Identity

### Matrix4x4::Init_Perspective
- Purpose: Initializes perspective projection matrix
- Calls: Make_Identity

### Matrix4x4::Transpose
- Purpose: Returns transposed matrix
- Calls: None

### Matrix4x4::Inverse
- Purpose: Computes matrix inverse using Gauss-Jordan elimination
- Calls: Swap, WWMath::Fabs

### operator* (Matrix4x4, Matrix4x4)
- Purpose: Matrix multiplication
- Calls: None

### operator* (Matrix4x4, Vector3)
- Purpose: Transforms Vector3 by matrix
- Calls: None

### operator* (Matrix4x4, Vector4)
- Purpose: Transforms Vector4 by matrix
- Calls: None

## Globals
None

## Dependencies
- vector4.h (Vector4 class)
- matrix3d.h (Matrix3D class)
- matrix3.h (Matrix3x3 class)
- always.h (WWINLINE, WWASSERT_PRINT)
- WWMath namespace (Fabs)
