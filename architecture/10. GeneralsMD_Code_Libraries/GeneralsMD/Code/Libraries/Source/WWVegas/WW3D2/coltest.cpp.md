# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/coltest.cpp

## Purpose
Implements collision test classes for axis-aligned and oriented bounding boxes in the SAGE engine.

## Responsibilities
- Defines `AABoxCollisionTestClass` for axis-aligned box collision tests
- Defines `OBBoxCollisionTestClass` for oriented bounding box collision tests
- Implements culling and transformation logic for collision detection
- Manages sweep bounding boxes for efficient collision checks

## Key Types
- `AABoxCollisionTestClass` (Class): Handles axis-aligned box collision tests with movement and rotation
- `OBBoxCollisionTestClass` (Class): Handles oriented bounding box collision tests with transformations
- `ROTATION_TYPE` (Enum): Defines rotation types (none, 90Â°, 180Â°, 270Â°)

## Key Functions
### `AABoxCollisionTestClass::Cull`
- Purpose: Checks if an axis-aligned box can be culled (no collision possible)
- Calls: `Vector3::Subtract`, `Vector3::Add`

### `AABoxCollisionTestClass::Rotate`
- Purpose: Rotates the collision test box by 90Â°, 180Â°, or 270Â° around Z-axis
- Calls: `Matrix3D::RotateZ90`, `Matrix3D::RotateZ180`, `Matrix3D::RotateZ270`, `Matrix3D::mulVector3Array`

### `AABoxCollisionTestClass::Transform`
- Purpose: Transforms the collision test box using a 3D transformation matrix
- Calls: `Matrix3D::Transform_Center_Extent_AABox`, `Matrix3D::Rotate_Vector`, `Matrix3D::mulVector3Array`

### `OBBoxCollisionTestClass::Cull`
- Purpose: Checks if an axis-aligned box can be culled against an oriented box
- Calls: `Vector3::Subtract`, `Vector3::Add`

## Globals
None

## Dependencies
- `coltest.h` (header)
- `Vector3`, `Matrix3D`, `AABoxClass`, `OBBoxClass`, `CollisionTestClass`, `CastResultStruct` (external types)
- `WWMath` (for absolute value calculations)
