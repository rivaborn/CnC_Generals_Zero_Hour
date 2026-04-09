# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathplane.cpp

## Purpose
Implements collision detection tests between various geometric primitives and planes.

## Responsibilities
- Tests overlap between AAPlane/Plane and points, lines, triangles, spheres, and boxes.
- Handles both axis-aligned and oriented bounding boxes.
- Uses epsilon-based comparisons for floating-point robustness.
- Provides utility functions for plane-based collision queries.

## Key Types
- `CollisionMath::OverlapType` (Enum): Result of overlap tests (POS, NEG, ON, BOTH).
- `AAPlaneClass` (Class): Axis-aligned plane representation.
- `PlaneClass` (Class): General plane representation.

## Key Functions
### `Overlap_Test(const AAPlaneClass &, const Vector3 &)`
- Purpose: Tests point-plane overlap.
- Calls: None.

### `Overlap_Test(const AAPlaneClass &, const LineSegClass &)`
- Purpose: Tests line-plane overlap.
- Calls: `Overlap_Test(AAPlaneClass, Vector3)` twice, `eval_overlap_mask`.

### `Overlap_Test(const PlaneClass &, const OBBoxClass &)`
- Purpose: Tests oriented box-plane overlap.
- Calls: `Matrix3x3::Transpose_Rotate_Vector`, `get_far_extent`, `Matrix3x3::Rotate_Vector`, `Overlap_Test(PlaneClass, Vector3)`.

## Globals
- `COINCIDENCE_EPSILON` (float): Tolerance for point-plane coincidence.
- `WWMATH_EPSILON` (float): General floating-point epsilon.

## Dependencies
- `colmath.h`, `colmathplane.h`, `aaplane.h`, `plane.h`, `lineseg.h`, `tri.h`, `sphere.h`, `aabox.h`, `
