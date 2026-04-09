# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathobbox.cpp

## Purpose
Implements collision detection functions for oriented bounding boxes (OBBox) against various geometric primitives.

## Responsibilities
- Tests overlap between OBBox and points, lines, triangles, AABox, and other OBBox.
- Computes collision results between OBBox and planes.
- Evaluates intersection results for overlap determination.

## Key Types
- `CollisionMath::OverlapType` (Enum): Result of overlap tests (INSIDE, OUTSIDE, BOTH).
- `CastResultStruct` (Struct): Stores collision results (fraction, normal, contact point).
- `OBBoxClass` (Class): Oriented bounding box with center, basis, and extent.
- `AABoxClass` (Class): Axis-aligned bounding box.
- `PlaneClass`, `LineSegClass`, `TriClass` (Classes): Geometric primitives for collision tests.

## Key Functions
### `Overlap_Test(const OBBoxClass &, const Vector3 &)`
- Purpose: Tests if a point is inside an OBBox.
- Calls: `Matrix3x3::Transpose_Rotate_Vector`, `WWMath::Fabs`.

### `Overlap_Test(const OBBoxClass &, const LineSegClass &)`
- Purpose: Tests overlap between an OBBox and a line segment.
- Calls: `Collide`, `eval_overlap_collision`.

### `Overlap_Test(const OBBoxClass &, const TriClass &)`
- Purpose: Tests overlap between an OBBox and a triangle.
- Calls: `Collide`, `eval_overlap_collision`.

### `Overlap_Test(const AABoxClass &, const OBBoxClass &)`
- Purpose: Tests overlap between an AABox and an OBBox.
- Calls: `CollisionMath::Intersection_Test`.

### `Collide(const
