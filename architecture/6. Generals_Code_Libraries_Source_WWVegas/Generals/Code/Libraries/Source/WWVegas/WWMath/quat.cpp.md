# Generals/Code/Libraries/Source/WWVegas/WWMath/quat.cpp

## Purpose
Implements quaternion mathematics for 3D rotations, including interpolation, conversion between quaternions and matrices, and trackball-style rotation.

## Responsibilities
- Quaternion construction and normalization
- Spherical linear interpolation (Slerp) for smooth rotations
- Conversion between quaternions and 3D/4D matrices
- Trackball rotation calculation for camera control
- Axis-angle to quaternion conversion

## Key Types
- Quaternion (Class): Represents a 3D rotation quaternion
- SlerpInfoStruct (Struct): Caches interpolation data for optimized Slerp
- Vector3 (Class): Used for axis vectors
- Matrix3D/Matrix3/Matrix4 (Classes): Matrix types for conversion

## Key Functions
### Quaternion::Quaternion(const Vector3 & axis, float angle)
- Purpose: Constructs a quaternion from an axis and rotation angle
- Calls: WWMath::Sin, WWMath::Cos

### Trackball(float x0, float y0, float x1, float y1, float sphsize)
- Purpose: Computes trackball rotation quaternion from 2D mouse coordinates
- Calls: project_to_sphere, Vector3::Cross_Product, Axis_To_Quat

### Slerp(Quaternion& res, const Quaternion & p, const Quaternion & q, float alpha)
- Purpose: Performs spherical linear interpolation between two quaternions
- Calls: WWMath::Acos, WWMath::Sin

### Build_Quaternion(const Matrix3D & mat)
- Purpose: Creates a quaternion from a 3D rotation matrix
- Calls: None (uses basic math)

### Build_Matrix3(const Quaternion & q)
- Purpose: Creates a 3x3 matrix from a quaternion
- Calls: None

## Globals
- _nxt (int[3]): Array for matrix index cycling (0â1â2â0)
- SLERP_EPSILON (float): Threshold for linear interpolation fallback

## Dependencies
- quat.h, matrix3d.h, matrix4.h, wwmath.h
- Vector3, Matrix3D, Matrix3, Matrix4 classes
- WWMath trigonometric functions (Sin, Cos, Acos, Sqrt, Inv_Sqrt, Asin)
- stdio.h, stdlib.h, math.h, assert.h
