# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathaabtri.cpp

## Purpose
Implements collision detection between axis-aligned bounding boxes (AABB) and triangles.

## Responsibilities
- Tests separation along multiple axes to determine collision
- Computes contact normals for collisions
- Provides both intersection tests and collision response calculations
- Optimized for AABB-triangle interactions using precomputed edge vectors

## Key Types
- BTCollisionStruct (Class): Holds scratchpad data for collision detection calculations
- AABTIntersectStruct (Class): Holds scratchpad data for intersection tests
- (anonymous enum) (Enum): Defines axis types for collision tests

## Key Functions
### aabtri_separation_test
- Purpose: Determines if objects are separated along a given axis
- Calls: None

### aabtri_check_axis
- Purpose: Projects AABB and triangle onto an arbitrary axis for separation test
- Calls: aabtri_separation_test, Vector3::Dot_Product

### aabtri_compute_contact_normal
- Purpose: Calculates the normal vector for a collision
- Calls: Vector3 operations, aabtri_check_axis variants

### CollisionMath::Intersection_Test
- Purpose: Tests if an AABB intersects with a triangle
- Calls: aabtri_intersect_* functions, Vector3::Cross_Product

## Globals
- CollisionContext (BTCollisionStruct): Static instance for collision calculations
- IntersectContext (AABTIntersectStruct): Static instance for intersection tests

## Dependencies
- colmath.h, aabox.h, tri.h, wwdebug.h
- Vector3 class operations
- WWMath namespace functions
- CollisionMath class (parent)
