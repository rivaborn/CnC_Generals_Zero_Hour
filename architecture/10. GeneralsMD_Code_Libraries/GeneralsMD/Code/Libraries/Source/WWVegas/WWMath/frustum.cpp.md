# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/frustum.cpp

## Purpose
Implements frustum initialization for view frustum calculations in the game engine.

## Responsibilities
- Initializes frustum from camera parameters
- Calculates frustum corners in camera and world space
- Generates frustum bounding planes
- Computes frustum bounding box

## Key Types
- `FrustumClass` (Class): Manages view frustum geometry and planes
- `Matrix3D` (Type): 3D transformation matrix
- `Vector2`/`Vector3` (Types): 2D/3D vectors
- `PlaneClass` (Class): Plane definition

## Key Functions
### `FrustumClass::Init`
- Purpose: Initializes frustum from camera transform and view plane parameters
- Calls: `Vector3::Cross_Product`, `Vector3::Dot_Product`, `Matrix3D::Transform_Vector`, `PlaneClass::Set`

## Globals
- None

## Dependencies
- `frustum.h` (header)
- `Matrix3D`, `Vector2`, `Vector3`, `PlaneClass` (external types)
