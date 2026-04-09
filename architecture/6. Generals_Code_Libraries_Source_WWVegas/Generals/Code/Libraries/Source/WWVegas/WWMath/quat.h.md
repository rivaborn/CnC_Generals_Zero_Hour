# Generals/Code/Libraries/Source/WWVegas/WWMath/quat.h

## Purpose
Defines the Quaternion class and related math operations for 3D rotations in the SAGE engine.

## Responsibilities
- Provides quaternion data structure and operations
- Supports quaternion-matrix conversions
- Implements spherical linear interpolation (Slerp)
- Offers rotation utilities (axis-angle, trackball)
- Includes quaternion validation and comparison

## Key Types
- **Quaternion (Class)**: Represents 3D rotations using quaternions (X,Y,Z imaginary parts, W real part)
- **SlerpInfoStruct (Struct)**: Caches data for optimized spherical interpolation between quaternions

## Key Functions
### Inverse
- Purpose: Computes the multiplicative inverse of a quaternion
- Calls: None

### Conjugate
- Purpose: Computes the conjugate of a quaternion
- Calls: None

### operator*
- Purpose: Multiplies two quaternions (composition of rotations)
- Calls: None

### Normalize
- Purpose: Returns a unit-length version of the quaternion
- Calls: Length()

### Slerp
- Purpose: Performs spherical linear interpolation between two quaternions
- Calls: None

### Build_Matrix3D
- Purpose: Converts a quaternion to a 3x3 rotation matrix
- Calls: None

### Equal_Within_Epsilon
- Purpose: Compares two quaternions with tolerance
- Calls: WWMath::Fabs()

## Globals
- None

## Dependencies
- "always.h", "wwmath.h", "matrix3.h", "vector3.h", "matrix3d.h"
- WWMath::Sqrt, WWMath::Is_Valid_Float, WWMath::Fabs
- Matrix3, Matrix3D, Matrix4, Vector3 classes
