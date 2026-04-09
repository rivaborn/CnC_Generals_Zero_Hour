# Generals/Code/Libraries/Source/WWVegas/WWMath/frustum.cpp

## Purpose
Implements frustum initialization for camera-based view frustum calculations in the SAGE engine.

## Responsibilities
- Initializes frustum geometry from camera transform and view plane parameters
- Handles reflected camera matrices by flipping frustum corners
- Computes frustum bounding planes and axis-aligned bounding box
- Transforms frustum corners from camera space to world space

## Key Types
- `FrustumClass`: Manages frustum geometry and planes
- `Matrix3D`: 3D transformation matrix
- `Vector2`: 2D vector
- `Vector3`: 3D vector
- `PlaneClass`: Frustum plane representation

## Key Functions
### `FrustumClass::Init`
- Purpose: Initializes frustum from camera transform and view plane parameters
- Calls:
  - `Vector3::Cross_Product`
  - `Vector3::Dot_Product`
  - `Matrix3D::Transform_Vector`
  - `PlaneClass::Set`

## Globals
None

## Dependencies
- `frustum.h` (header)
- `Vector2`, `Vector3`, `Matrix3D`, `PlaneClass` (external math types)
