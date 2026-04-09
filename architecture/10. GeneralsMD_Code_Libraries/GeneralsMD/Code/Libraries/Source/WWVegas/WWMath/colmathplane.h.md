# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathplane.h

## Purpose
Provides inline collision detection functions for planes, including overlap tests with points and axis-aligned bounding boxes.

## Responsibilities
- Defines `get_far_extent` to compute box extents along a plane normal.
- Implements `CollisionMath::Overlap_Test` for plane-point and plane-AABox overlap checks.
- Uses epsilon-based comparisons for robust floating-point collision detection.

## Key Types
- `CollisionMath::OverlapType` (Enum): Result of overlap tests (POS/NEG/ON/BOTH).

## Key Functions
### `get_far_extent`
- Purpose: Computes the farthest point of a box along a given normal.
- Calls: `WWMath::Fast_Is_Float_Positive`.

### `CollisionMath::Overlap_Test(PlaneClass, Vector3)`
- Purpose: Tests overlap between a plane and a point.
- Calls: `Vector3::Dot_Product`.

### `CollisionMath::Overlap_Test(PlaneClass, AABoxClass)`
- Purpose: Tests overlap between a plane and an axis-aligned box.
- Calls: `get_far_extent`, `CollisionMath::Overlap_Test(PlaneClass, Vector3)`.

## Globals
- `COINCIDENCE_EPSILON` (float): Tolerance for floating-point comparisons.

## Dependencies
- `always.h`, `plane.h`, `aabox.h`
- `Vector3`, `WWMath`, `CollisionMath` (external).
