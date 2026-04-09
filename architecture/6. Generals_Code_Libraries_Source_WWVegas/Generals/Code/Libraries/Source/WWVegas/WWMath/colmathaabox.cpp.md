# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathaabox.cpp

## Purpose
Implements collision detection algorithms for Axis-Aligned Bounding Boxes (AABBs) in the SAGE engine.

## Responsibilities
- Tests intersection between two AABBs
- Tests overlap between AABBs and other primitives (spheres, triangles, line segments)
- Handles collision detection for moving AABBs against planes
- Implements sweeping collision tests for moving AABBs

## Key Types
- **AABCollisionStruct (Class)**: Holds intermediate data for AABB collision tests
- **CollisionMath (Namespace)**: Contains static collision detection methods

## Key Functions
### CollisionMath::Intersection_Test
- Purpose: Tests if two AABBs intersect
- Calls: None

### CollisionMath::Overlap_Test (variants)
- Purpose: Tests overlap between AABB and sphere/triangle/line segment
- Calls: Other Overlap_Test variants, CollisionMath::Collide

### CollisionMath::Collide (variants)
- Purpose: Tests collision between moving AABBs or AABB and plane
- Calls: aab_separation_test, Vector3 operations

### aab_separation_test
- Purpose: Tests separation between two AABBs along a specific axis
- Calls: None

## Globals
- None

## Dependencies
- Key includes: colmath.h, colmathinlines.h, aaplane.h, plane.h, lineseg.h, tri.h, sphere.h, aabox.h, obbox.h, wwdebug.h
- External symbols: Vector3, WWMath, CollisionMath namespace methods
