# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/matrix3.h

## Purpose
Defines the Matrix3x3 class and related mathematical operations for 3D transformations in the SAGE engine.

## Responsibilities
- Provides 3x3 matrix operations (addition, subtraction, multiplication)
- Supports matrix-vector multiplication for transformations
- Implements rotation matrices and quaternion conversions
- Includes matrix utilities (transpose, inverse, determinant)
- Manages axis-aligned bounding box transformations

## Key Types
- Matrix3x3 (Class): 3x3 transformation matrix with vector rows
- Matrix3D (Class): Forward declaration for 3D matrix compatibility
- Matrix4x4 (Class): Forward declaration for 4x4 matrix compatibility
- Quaternion (Class): Forward declaration for quaternion support

## Key Functions
### Matrix3x3::Rotate_X/Y/Z
- Purpose: Post-multiplies rotation about specified axis
- Calls: sinf, cosf

### Create_X/Y/Z_Rotation_Matrix3
- Purpose: Creates rotation matrices for specified axes
- Calls: sinf, cosf

### operator* (Matrix3x3 Ã Matrix3x3)
- Purpose: Matrix multiplication
- Calls: None (direct computation)

### operator* (Matrix3x3 Ã Vector3)
- Purpose: Transforms vector by matrix
- Calls: None (direct computation)

## Globals
- Matrix3x3::Identity (Matrix3x3): Identity matrix constant
- Matrix3x3::RotateX90/180/270 (Matrix3x3): Predefined X-axis rotation matrices
- Matrix3x3::RotateY90/180/270 (Matrix3x3): Predefined Y-axis rotation matrices
- Matrix3x3::RotateZ90/180/270 (Matrix3x3): Predefined Z-axis rotation matrices

## Dependencies
- "vector3.h": Vector3 class usage
- "wwdebug.h": Assertion macros
- "always.h": Platform-specific macros
- sinf, cosf: Math library functions
- WWMath::Fabs: Absolute value function
