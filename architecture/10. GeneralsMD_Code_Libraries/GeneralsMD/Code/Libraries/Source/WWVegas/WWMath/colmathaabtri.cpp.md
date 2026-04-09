# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathaabtri.cpp

## Purpose
Implements collision detection between axis-aligned bounding boxes (AABB) and triangles.

## Responsibilities
- Tests separation along multiple axes to detect collision
- Computes contact normals for collisions
- Provides both static intersection tests and dynamic collision tests
- Uses optimized projections for AABB-triangle interactions

## Key Types
- (anonymous enum) (Enum): Defines axis types for collision tests
- BTCollisionStruct (Class): Scratchpad for collision detection calculations
- AABTIntersectStruct (Class): Scratchpad for intersection tests

## Key Functions
### aabtri_separation_test
- Purpose: Determines if objects are separated along an axis
- Calls: None

### aabtri_check_axis
- Purpose: Projects AABB and triangle onto arbitrary axis for separation test
- Calls: aabtri_separation_test, Vector3::Dot_Product

### aabtri_compute_contact_normal
- Purpose: Computes collision normal when objects intersect
- Calls: Vector3 operations, WWMath functions

### CollisionMath::Intersection_Test
- Purpose: Tests if AABB and triangle intersect
- Calls: aabtri_intersect_* functions, Vector3::Cross_Product

## Globals
- CollisionContext (BTCollisionStruct): Static scratchpad for collision detection
- IntersectContext (AABTIntersectStruct): Static scratchpad for intersection tests

## Dependencies
- colmath.h, aabox.h, tri.h, wwdebug.h
- Vector3 class operations
- WWMath functions and constants
