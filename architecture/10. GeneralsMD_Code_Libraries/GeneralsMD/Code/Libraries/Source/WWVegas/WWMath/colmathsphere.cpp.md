# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathsphere.cpp

## Purpose
Implements collision detection functions for spheres against various geometric primitives.

## Responsibilities
- Sphere-AABox intersection test
- Sphere-OBBox intersection test
- Sphere overlap tests (point, line, triangle, sphere, AABox, OBBox)

## Key Types
- `CollisionMath` (Class): Namespace for collision detection utilities
- `SphereClass` (Class): Represents a sphere in 3D space
- `AABoxClass` (Class): Axis-aligned bounding box
- `OBBoxClass` (Class): Oriented bounding box
- `OverlapType` (Enum): Result of overlap tests (NEG, POS, ON, OUTSIDE, INSIDE, OVERLAPPED, BOTH)

## Key Functions
### `Intersection_Test(const SphereClass &, const AABoxClass &)`
- Purpose: Tests if a sphere intersects an axis-aligned bounding box
- Calls: `WWMath::Fabs`

### `Intersection_Test(const SphereClass &, const OBBoxClass &)`
- Purpose: Tests if a sphere intersects an oriented bounding box
- Calls: `Matrix3D::Inverse_Transform_Vector`, `WWMath::Fabs`

### `Overlap_Test(const SphereClass &, const Vector3 &)`
- Purpose: Tests overlap between a sphere and a point
- Calls: `Vector3::Length2`

### `Overlap_Test(const SphereClass &, const SphereClass &)`
- Purpose: Tests overlap between two spheres
- Calls: `Vector3::Length2`

### `Overlap_Test(const SphereClass &, const AABoxClass &)`
- Purpose: Tests overlap between a sphere and an axis-aligned box
- Calls: `Intersection_Test`

### `Overlap_Test(const SphereClass &, const OBBoxClass &)`
- Purpose: Tests overlap between a sphere and an oriented box
- Calls: `Intersection_Test`

## Globals
- `COINCIDENCE_EPSILON` (float): Tolerance value for floating-point comparisons

## Dependencies
- `colmath.h`, `aaplane.h`, `plane.h`, `lineseg.h`, `tri.h`, `sphere.h`, `aabox.h`, `obbox.h`, `wwdebug.h`
- `Vector3`, `Matrix3D`, `WWMath`
