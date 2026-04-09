# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathfrustum.h

## Purpose
Provides inline collision detection functions for frustums in the WWMath library.

## Responsibilities
- Defines collision testing between frustums and axis-aligned bounding boxes (AABB).
- Implements frustum-plane overlap checks.
- Uses bitmask optimization to skip redundant plane tests.

## Key Types
- `CollisionMath::OverlapType` (Enum): Result of overlap test (INSIDE, OUTSIDE, OVERLAPPED).
- `FrustumClass` (Class): Frustum geometry container.
- `AABoxClass` (Class): Axis-aligned bounding box.

## Key Functions
### `CollisionMath::Overlap_Test`
- Purpose: Tests overlap between a frustum and an AABB.
- Calls:
  - `CollisionMath::Overlap_Test` (recursively for each frustum plane).

## Globals
None

## Dependencies
- `always.h`, `aabox.h`, `vector3.h`, `lineseg.h`, `frustum.h`
- `CollisionMath` namespace (external)
- `INSIDE`, `OUTSIDE`, `OVERLAPPED` constants (external)
