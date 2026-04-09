# Generals/Code/Libraries/Source/WWVegas/WWMath/matrix3.h

## Purpose
Header file defining the Matrix3 class and related 3x3 matrix operations for 3D transformations.

## Responsibilities
- Provides 3x3 matrix class for 3D transformations
- Implements matrix arithmetic (addition, subtraction, multiplication)
- Supports rotation operations and matrix decomposition
- Includes utility functions for matrix creation and manipulation

## Key Types
- Matrix3 (Class): 3x3 transformation matrix with vector rows
- Matrix3D (Class): Forward declaration for 3x4 matrix compatibility
- Matrix4 (Class): Forward declaration for 4x4 matrix compatibility
- Quaternion (Class): Forward declaration for quaternion conversion

## Key Functions
### Matrix3::Matrix3(bool identity)
- Purpose: Constructor that optionally initializes to identity matrix
- Calls: None

### Matrix3::Transpose()
- Purpose: Returns transpose of the matrix
- Calls: None

### Matrix3::Inverse()
- Purpose: Returns the inverse of the matrix
- Calls: None

### Matrix3::Rotate_X(float theta)
- Purpose: Post-multiplies an X-axis rotation onto the current matrix
- Calls: Rotate_X(float s, float c)

### Create_X_Rotation_Matrix3(float rad)
- Purpose: Creates a rotation matrix about the X-axis
- Calls: Create_X_Rotation_Matrix3(float s, float c)

### operator*(const Matrix3& a, const Vector3& v)
- Purpose: Multiplies matrix by vector
- Calls: None

## Globals
- Identity (Matrix3): Pre-initialized identity matrix
- RotateX90, RotateX180, RotateX270 (Matrix3): Pre-initialized X-axis rotation matrices
- RotateY90, RotateY180, RotateY270 (Matrix3): Pre-initialized Y-axis rotation matrices
- RotateZ90, RotateZ180, RotateZ270 (Matrix3): Pre-initialized Z-axis rotation matrices

## Dependencies
- "always.h": WWINLINE macro definition
- "vector3.h": Vector3 class definition
- "wwdebug.h": Debug assertion macros
- "osdep.h": Platform-specific definitions (Unix)
