# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathfrustum.cpp

## Purpose
Implements collision detection functions for frustums against various geometric primitives.

## Responsibilities
- Tests overlap between frustums and points, triangles, spheres, and axis-aligned/oriented bounding boxes
- Determines if primitives are inside, outside, or overlapping with a frustum
- Optimizes plane checks for oriented bounding boxes using a bitmask

## Key Types
- `CollisionMath::OverlapType` (Enum): Result of overlap tests (INSIDE, OUTSIDE, OVERLAPPED)
- `FrustumClass` (Class): Frustum geometry container (used but not defined here)
- `Vector3` (Struct): 3D point (used but not defined here)
- `TriClass`, `SphereClass`, `AABoxClass`, `OBBoxClass` (Classes): Geometric primitives (used but not defined here)

## Key Functions
### `Overlap_Test(const FrustumClass &, const Vector3 &)`
- Purpose: Tests if a point is inside, outside, or overlapping with a frustum
- Calls: `CollisionMath::Overlap_Test` for each frustum plane

### `Overlap_Test(const FrustumClass &, const TriClass &)`
- Purpose: Tests if a triangle overlaps with a frustum
- Calls: `CollisionMath::Overlap_Test` for each frustum plane

### `Overlap_Test(const FrustumClass &, const SphereClass &)`
- Purpose: Tests if a sphere overlaps with a frustum
- Calls: `CollisionMath::Overlap_Test` for each frustum plane

### `Overlap_Test(const FrustumClass &, const AABoxClass &)`
- Purpose: Tests if an axis-aligned box overlaps with a frustum
- Calls: `
