# Generals/Code/Tools/WW3D/pluglib/matrix4.h

## Purpose
Defines a 4x4 matrix class for 3D transformations, including projection matrices and matrix operations.

## Responsibilities
- Provides 4x4 matrix operations (addition, subtraction, multiplication)
- Supports matrix initialization (identity, orthographic, perspective)
- Implements matrix transformations (transpose, inverse)
- Handles vector-matrix multiplication
- Manages matrix comparison and assignment

## Key Types
- **Matrix4 (Class)**: Represents a 4x4 transformation matrix with row-major storage

## Key Functions
### Matrix4::Inverse
- Purpose: Computes the matrix inverse using Gauss-Jordan elimination
- Calls: `Swap`, `WWMath::Fabs`

### Matrix4::Init_Perspective
- Purpose: Initializes a perspective projection matrix
- Calls: `Make_Identity`

### operator* (Matrix4, Matrix4)
- Purpose: Multiplies two matrices
- Calls: None (inline computation)

### operator* (Matrix4, Vector3)
- Purpose: Transforms a 3D vector by the matrix
- Calls: None (inline computation)

## Globals
- None

## Dependencies
- `vector4.h`, `matrix3d.h`, `wwmatrix3.h`
- `WWMath::Fabs` (external)
- `Swap` (external)
