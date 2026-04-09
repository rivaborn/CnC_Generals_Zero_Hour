# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathplane.cpp

## Purpose
Implements collision detection functions for axis-aligned and oriented planes against various geometric primitives.

## Responsibilities
- Tests overlap between planes and points, lines, triangles, spheres, and boxes
- Handles both axis-aligned (AAPlaneClass) and oriented (PlaneClass) planes
- Uses bitmask evaluation for overlap determination
- Provides specialized logic for oriented bounding boxes (OBBoxClass)

## Key Types
- `AAPlaneClass`: Axis-aligned plane representation
- `PlaneClass`: Oriented plane representation
- `OverlapType` (enum): Result of overlap tests (POS/NEG/ON/BOTH)

## Key Functions
### `Overlap_Test(AAPlaneClass, Vector3)`
- Purpose: Tests point-plane overlap for axis-aligned planes
- Calls: None

### `Overlap_Test(PlaneClass, SphereClass)`
- Purpose: Tests sphere-plane overlap for oriented planes
- Calls: `Vector3::Dot_Product`

### `Overlap_Test(PlaneClass, OBBoxClass)`
- Purpose: Tests oriented box-plane overlap
- Calls: `Matrix3::Transpose_Rotate_Vector`, `Matrix3::Rotate_Vector`, `get_far_extent`

## Globals
- `COINCIDENCE_EPSILON` (float): Tolerance for point-plane coincidence
- `WWMATH_EPSILON` (float): General math tolerance

## Dependencies
- `colmath.h`, `colmathplane.h`, `aaplane.h`, `plane.h`, `lineseg.h`, `tri.h`, `sphere.h`, `aabox.h`, `obbox.h`, `wwdebug.h`
- `Vector3`, `Matrix3`, `AAPlaneClass`, `PlaneClass`, `LineSeg
