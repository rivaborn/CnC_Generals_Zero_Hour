# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/quat.cpp

## Purpose
Implements quaternion mathematics for 3D rotations, including interpolation, conversion between quaternions and matrices, and trackball-style rotation.

## Responsibilities
- Quaternion construction and normalization
- Spherical linear interpolation (Slerp) for smooth rotations
- Conversion between quaternions and 3D matrices
- Trackball-style rotation calculations
- Axis-angle to quaternion conversion

## Key Types
- Quaternion (class): 4D rotation representation
- SlerpInfoStruct (struct): Cached interpolation data
- Vector3 (class): 3D vector used in calculations

## Key Functions
### Quaternion::Quaternion(const Vector3 & axis, float angle)
- Purpose: Constructs a quaternion from axis-angle representation
- Calls: WWMath::Sin, WWMath::Cos

### Trackball(float x0, float y0, float x1, float y1, float sphsize)
- Purpose: Computes trackball rotation quaternion from mouse coordinates
- Calls: project_to_sphere, Vector3::Cross_Product, Axis_To_Quat

### Slerp(const Quaternion & p, const Quaternion & q, float alpha, Quaternion & res)
- Purpose: Performs spherical linear interpolation between two quaternions
- Calls: WWMath::Acos, WWMath::Sin

### Build_Quaternion(const Matrix3D & mat)
- Purpose: Creates quaternion from rotation matrix
- Calls: None (uses basic math)

### Build_Matrix3(const Quaternion & q)
- Purpose: Creates 3x3 matrix from quaternion
- Calls: None

## Globals
- _nxt (int[3]): Array for matrix index cycling
- SLERP_EPSILON (float): Threshold for linear interpolation fallback

## Dependencies
- quat.h, matrix3d.h, matrix4.h, wwmath.h
- Vector3, Matrix3D, Matrix3x3, Matrix4x4 classes
- WWMath trigonometric functions (Sin, Cos, Acos, Sqrt, Inv_Sqrt)
