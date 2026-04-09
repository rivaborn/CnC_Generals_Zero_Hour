# Generals/Code/Tools/WW3D/pluglib/w3dquat.h

## Purpose
Defines the Quaternion class and related utilities for 3D rotation operations in the W3D engine.

## Responsibilities
- Provides quaternion data structure and operations
- Supports quaternion-matrix conversions
- Implements spherical linear interpolation (slerp)
- Offers trackball-style rotation calculations
- Includes quaternion validation and normalization

## Key Types
- **Quaternion (Class)**: Represents 3D rotations using quaternions (X,Y,Z imaginary parts, W real part)
- **SlerpInfoStruct (Struct)**: Caches intermediate values for optimized spherical interpolation

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
- Purpose: Returns a unit-length version of a quaternion
- Calls: Length()

### Slerp
- Purpose: Performs spherical linear interpolation between two quaternions
- Calls: Not inferable

### Build_Matrix3
- Purpose: Converts a quaternion to a 3x3 rotation matrix
- Calls: Not inferable

## Globals
- None

## Dependencies
- "always.h", "wwmath.h", "wwmatrix3.h", "vector3.h"
- WWMath::Sqrt, WWMath::Is_Valid_Float
- Matrix3, Matrix3D, Matrix4, Vector3 classes
