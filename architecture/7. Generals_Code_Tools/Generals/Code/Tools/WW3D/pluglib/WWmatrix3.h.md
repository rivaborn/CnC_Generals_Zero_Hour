# Generals/Code/Tools/WW3D/pluglib/WWmatrix3.h

## Purpose
Defines the Matrix3 class and related 3D matrix operations for the WW3D engine.

## Responsibilities
- Provides 3x3 matrix operations for 3D transformations
- Supports matrix arithmetic, rotations, and vector transformations
- Includes utility functions for creating rotation matrices

## Key Types
- Matrix3 (Class): 3x3 transformation matrix with rotation/transformation operations
- Matrix3D (Class): Forward declaration for 4x4 matrix compatibility
- Matrix4 (Class): Forward declaration for 4x4 matrix compatibility
- Quaternion (Class): Forward declaration for quaternion compatibility

## Key Functions
### Matrix3::Rotate_X
- Purpose: Post-multiplies an X-axis rotation onto the current matrix
- Calls: Rotate_X(float s,float c)

### Matrix3::Rotate_Y
- Purpose: Post-multiplies a Y-axis rotation onto the current matrix
- Calls: Rotate_Y(float s,float c)

### Matrix3::Rotate_Z
- Purpose: Post-multiplies a Z-axis rotation onto the current matrix
- Calls: Rotate_Z(float s,float c)

### Create_X_Rotation_Matrix3
- Purpose: Creates a rotation matrix around the X-axis
- Calls: Create_X_Rotation_Matrix3(float s,float c)

### Create_Y_Rotation_Matrix3
- Purpose: Creates a rotation matrix around the Y-axis
- Calls: Create_Y_Rotation_Matrix3(float s,float c)

### Create_Z_Rotation_Matrix3
- Purpose: Creates a rotation matrix around the Z-axis
- Calls: Create_Z_Rotation_Matrix3(float s,float c)

## Globals
- None

## Dependencies
- "always.h"
- "vector3.h"
- Matrix3D, Matrix4, Quaternion (forward declarations)
