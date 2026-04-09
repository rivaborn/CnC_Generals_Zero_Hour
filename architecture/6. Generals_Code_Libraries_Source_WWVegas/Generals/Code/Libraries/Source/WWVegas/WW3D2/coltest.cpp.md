# Generals/Code/Libraries/Source/WWVegas/WW3D2/coltest.cpp

## Purpose
Implements collision test classes for axis-aligned and oriented bounding boxes in the SAGE engine.

## Responsibilities
- Defines `AABoxCollisionTestClass` for axis-aligned box collision tests
- Defines `OBBoxCollisionTestClass` for oriented bounding box collision tests
- Implements culling and transformation logic for collision detection
- Handles 90-degree rotations about the Z-axis for axis-aligned boxes

## Key Types
- `AABoxCollisionTestClass` (Class): Tests collision for axis-aligned bounding boxes with movement
- `OBBoxCollisionTestClass` (Class): Tests collision for oriented bounding boxes with movement
- `CollisionTestClass` (Base Class): Abstract base class for collision tests
- `AABoxClass` (External): Axis-aligned bounding box structure
- `OBBoxClass` (External): Oriented bounding box structure
- `Vector3` (External): 3D vector math structure
- `Matrix3D` (External): 3D transformation matrix
- `CastResultStruct` (External): Stores collision test results
- `ROTATION_TYPE` (Enum): Defines rotation types (none, 90Â°, 180Â°, 270Â°)

## Key Functions
### `AABoxCollisionTestClass::Cull`
- Purpose: Determines if an axis-aligned box can be culled (no collision possible)
- Calls: `Vector3::Subtract`, `Vector3::Add`

### `AABoxCollisionTestClass::Rotate`
- Purpose: Rotates the collision test box by 90Â°, 180Â°, or 270Â° about the Z-axis
- Calls: `Matrix3D::RotateZ90`, `Matrix3D::RotateZ180`, `Matrix3D::RotateZ270`, `Matrix3D::mulVector3`, `Matrix3D::mulVector3Array`

### `AABoxCollisionTestClass::Transform`
- Purpose: Transforms the collision test box by an arbitrary matrix
- Calls: `Matrix3D::Transform_Center_Extent_AABox`, `Matrix3D::Rotate_Vector`, `Matrix3D::mulVector3Array`

### `OBBoxCollisionTestClass::Cull`
- Purpose: Determines if an oriented bounding box can be culled (no collision possible)
- Calls: `Vector3::Subtract`, `Vector3::Add`

## Globals
None

## Dependencies
- `coltest.h` (header)
- `Vector3`, `Matrix3D`, `AABoxClass`, `OBBoxClass`, `CastResultStruct` (from WW3D math library)
- `WWMath` (for floating
