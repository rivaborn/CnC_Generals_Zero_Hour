# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathfrustum.h

## Purpose
Provides collision detection functions for frustums and axis-aligned bounding boxes (AABB).

## Responsibilities
- Defines inline collision test for frustum-AABB overlap
- Uses frustum planes to determine spatial relationships
- Tracks which planes have been tested via bitmask

## Key Types
- None

## Key Functions
### CollisionMath::Overlap_Test
- Purpose: Tests overlap between a frustum and an AABB
- Calls: CollisionMath::Overlap_Test (plane-AABB test)

## Globals
- None

## Dependencies
- "always.h", "aabox.h", "vector3.h", "lineseg.h", "frustum.h"
- CollisionMath namespace
- FrustumClass, AABoxClass, OverlapType (INSIDE, OUTSIDE, OVERLAPPED)
