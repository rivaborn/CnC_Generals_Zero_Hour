# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/inttest.h

## Purpose
Defines classes for performing intersection tests between geometric primitives in 3D space.

## Responsibilities
- Provides base class for intersection tests (`IntersectionTestClass`)
- Implements axis-aligned box intersection tests (`AABoxIntersectionTestClass`)
- Implements oriented bounding box intersection tests (`OBBoxIntersectionTestClass`)
- Includes culling and triangle intersection methods

## Key Types
- **IntersectionTestClass (Class)**: Base class for intersection tests, stores collision type
- **AABoxIntersectionTestClass (Class)**: Axis-aligned box intersection test
- **OBBoxIntersectionTestClass (Class)**: Oriented bounding box intersection test

## Key Functions
### AABoxIntersectionTestClass::Cull(const Vector3 &, const Vector3 &)
- Purpose: Cull against another axis-aligned box defined by min/max vectors
- Calls: `Vector3::Subtract`, `Vector3::Add`

### AABoxIntersectionTestClass::Cull(const AABoxClass &)
- Purpose: Cull against another axis-aligned box
- Calls: `Vector3::Subtract`, `Vector3::Add`, `WWMath::Fabs`

### AABoxIntersectionTestClass::Intersect_Triangle(const TriClass &)
- Purpose: Test intersection with a triangle
- Calls: `CollisionMath::Intersection_Test`

### OBBoxIntersectionTestClass::update_bounding_box()
- Purpose: Updates the axis-aligned bounding box for the oriented box
- Calls: `Box.Basis.Rotate_AABox_Extent`

## Globals
None

## Dependencies
- `always.h`, `aabox.h`, `obbox.h`, `tri.h`, `colmath.h`, `coltype.h`
- `Vector3`, `Matrix3D`, `WWMath`, `CollisionMath`
