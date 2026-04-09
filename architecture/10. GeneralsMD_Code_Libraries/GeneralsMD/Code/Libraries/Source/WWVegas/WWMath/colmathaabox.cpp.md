# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathaabox.cpp

## Purpose
Implements collision detection functions for Axis-Aligned Bounding Boxes (AABBs) in the WWMath library.

## Responsibilities
- Tests intersection between two AABBs
- Tests overlap between AABBs and other primitives (spheres, triangles, line segments)
- Performs collision tests for moving AABBs against planes and other AABBs
- Computes collision results including contact points and normals

## Key Types
- **AABCollisionStruct (Class)**: Contains intermediate values for AABB collision detection
- **CollisionMath (Namespace)**: Contains static collision detection methods

## Key Functions
### CollisionMath::Intersection_Test
- Purpose: Tests if two AABBs intersect
- Calls: None

### CollisionMath::Overlap_Test (variants)
- Purpose: Tests overlap between AABB and sphere/triangle/line segment
- Calls: CollisionMath::Collide, Vector3 operations

### CollisionMath::Collide (variants)
- Purpose: Tests collision between moving AABBs and other primitives
- Calls: aab_separation_test, Vector3 operations

### aab_separation_test
- Purpose: Tests two AABBs for separation on an axis
- Calls: None

## Globals
- None

## Dependencies
- Key includes: colmath.h, colmathinlines.h, aaplane.h, plane.h, lineseg.h, tri.h, sphere.h, aabox.h, obbox.h, wwdebug.h
- External symbols: Vector3, WWMath, WWDEBUG_SAY
