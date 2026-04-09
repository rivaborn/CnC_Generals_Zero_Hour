# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathobbox.cpp

## Purpose
Implements collision detection functions for oriented bounding boxes (OBBox) against various geometric primitives.

## Responsibilities
- Tests overlap between OBBox and points, lines, triangles, AABox, and other OBBox.
- Computes collision results between OBBox and planes.
- Handles coordinate transformations for OBBox collision tests.

## Key Types
- `OBBoxClass`: Oriented bounding box with center, basis, and extent.
- `OverlapType` (enum): Result of overlap test (INSIDE, OUTSIDE, BOTH).
- `CastResultStruct`: Stores collision results (fraction, normal, contact point).

## Key Functions
### `Overlap_Test(const OBBoxClass &, const Vector3 &)`
- Purpose: Tests if a point is inside an OBBox.
- Calls: `Matrix3::Transpose_Rotate_Vector`

### `Overlap_Test(const OBBoxClass &, const LineSegClass &)`
- Purpose: Tests overlap between OBBox and a line segment.
- Calls: `Collide`, `eval_overlap_collision`

### `Collide(const OBBoxClass &, const Vector3 &, const PlaneClass &, CastResultStruct *)`
- Purpose: Computes collision between OBBox and a plane with movement.
- Calls: `Vector3::Dot_Product`, `box.Project_To_Axis`

## Globals
None

## Dependencies
- `colmath.h`, `aaplane.h`, `plane.h`, `lineseg.h`, `tri.h`, `sphere.h`, `aabox.h`, `obbox.h`, `wwdebug.h`
- `CollisionMath`, `Matrix3`, `Vector3`, `AABoxClass`, `TriClass`, `LineSegClass`, `PlaneClass`
