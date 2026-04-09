# Generals/Code/Tools/WW3D/pluglib/w3dquat.cpp

## Purpose
Implements quaternion mathematics for 3D transformations, including interpolation, conversion between quaternions and matrices, and trackball rotation.

## Responsibilities
- Quaternion construction and manipulation
- Spherical linear interpolation (Slerp)
- Conversion between quaternions and transformation matrices
- Trackball rotation calculations
- Quaternion normalization and randomization

## Key Types
- Quaternion (Class): Represents a 3D rotation quaternion
- SlerpInfoStruct (Struct): Stores precomputed values for optimized Slerp operations
- Vector3 (Class): 3D vector used for axis calculations

## Key Functions
### Quaternion::Quaternion(const Vector3 & axis, float angle)
- Purpose: Constructs a quaternion from an axis and rotation angle
- Calls: None

### Trackball(float x0, float y0, float x1, float y1, float sphsize)
- Purpose: Computes trackball rotation quaternion from mouse coordinates
- Calls: project_to_sphere, Vector3::Cross_Product, Axis_To_Quat

### Slerp(const Quaternion & p, const Quaternion & q, float alpha)
- Purpose: Performs spherical linear interpolation between two quaternions
- Calls: None

### Build_Quaternion(const Matrix3D & mat)
- Purpose: Creates a quaternion from a 3D transformation matrix
- Calls: None

### Build_Matrix3(const Quaternion & q)
- Purpose: Creates a 3x3 matrix from a quaternion
- Calls: None

## Globals
- _nxt (int[3]): Array for matrix index cycling (0â1â2â0)

## Dependencies
- w3dquat.h, matrix3d.h, matrix4.h, wwmath.h
- Vector3 class operations
- WWMath::Sqrt function
- Standard C math library functions
