# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathfrustum.cpp

## Purpose
Implements collision detection functions for frustums against various geometric primitives.

## Responsibilities
- Tests overlap between frustums and points, triangles, spheres, and boxes
- Determines if primitives are inside, outside, or overlapping with frustums
- Optimizes plane checks for oriented bounding boxes

## Key Types
- None

## Key Functions
### Overlap_Test(frustum, point)
- Purpose: Tests if a point is inside, outside, or overlapping with a frustum
- Calls: `CollisionMath::Overlap_Test` (plane-point)

### Overlap_Test(frustum, tri)
- Purpose: Tests if a triangle overlaps with a frustum
- Calls: `CollisionMath::Overlap_Test` (plane-triangle)

### Overlap_Test(frustum, sphere)
- Purpose: Tests if a sphere overlaps with a frustum
- Calls: `CollisionMath::Overlap_Test` (plane-sphere)

### Overlap_Test(frustum, AABoxClass)
- Purpose: Tests if an axis-aligned box overlaps with a frustum
- Calls: `CollisionMath::Overlap_Test` (plane-AABox)

### Overlap_Test(frustum, OBBoxClass)
- Purpose: Tests if an oriented bounding box overlaps with a frustum
- Calls: `CollisionMath::Overlap_Test` (plane-OBBox)

### Overlap_Test(frustum, OBBoxClass, planes_passed)
- Purpose: Optimized overlap test for OBBox with plane caching
- Calls: `CollisionMath::Overlap_Test` (plane-OBBox)

## Globals
- None

## Dependencies
- `colmath.h`, `colmathinlines.h`, `aaplane.h`, `plane.h`, `linese
