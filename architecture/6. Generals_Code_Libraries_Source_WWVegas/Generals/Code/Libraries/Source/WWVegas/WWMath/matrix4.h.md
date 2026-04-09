# Generals/Code/Libraries/Source/WWVegas/WWMath/matrix4.h

## Purpose
Defines the Matrix4 class for 4x4 matrix operations used in 3D transformations and projections.

## Responsibilities
- Provides 4x4 matrix arithmetic (addition, subtraction, multiplication)
- Supports matrix-vector transformations
- Implements projection matrices (orthographic, perspective)
- Handles matrix operations like transpose and inverse
- Supports conversion from Matrix3D and Matrix3 types

## Key Types
- Matrix4 (Class): 4x4 transformation matrix with row-major storage
- Vector4 (Class): Used as matrix rows (external dependency)

## Key Functions
### Matrix4::Inverse
- Purpose: Computes matrix inverse using Gauss-Jordan elimination
- Calls: Swap, WWMath::Fabs

### Matrix4::Init_Perspective
- Purpose: Initializes perspective projection matrix
- Calls: Make_Identity

### operator* (Matrix4, Matrix4)
- Purpose: Matrix multiplication
- Calls: None (direct computation)

### Transform_Vector
- Purpose: Transforms vectors using matrix
- Calls: None (direct computation)

## Globals
None

## Dependencies
- vector4.h (Vector4 class)
- matrix3d.h (Matrix3D class)
- matrix3.h (Matrix3 class)
- always.h (WWINLINE macro)
- WWMath namespace (Fabs function)
