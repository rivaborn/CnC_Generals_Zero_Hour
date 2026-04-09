# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathobbtri.cpp

## Purpose
Implements collision detection between oriented bounding boxes (OBBox) and triangles, including both intersection tests and collision response calculations.

## Responsibilities
- Tests separation between OBBox and triangle along multiple axes
- Computes collision contact points and normals
- Performs intersection checks between OBBox and triangle
- Handles both static and dynamic collision scenarios

## Key Types
- BTCollisionStruct (Class): Context structure for collision detection calculations
- BTIntersectStruct (Class): Context structure for intersection tests
- (anonymous enum) (Enum): Defines axis types for collision tests

## Key Functions
### obbtri_collision_separation_test
- Purpose: Tests if objects are separated along a given axis
- Calls: None

### obbtri_check_collision_axis
- Purpose: Projects objects onto arbitrary axis and tests for separation
- Calls: obbtri_collision_separation_test

### obbtri_compute_contact_normal
- Purpose: Computes the normal vector for collision contact
- Calls: None

### obbtri_compute_contact_point
- Purpose: Calculates the contact point between colliding objects
- Calls: eval_A0_point, eval_A1_point, eval_A2_point

### CollisionMath::Intersection_Test
- Purpose: Tests if OBBox intersects with triangle
- Calls: obbtri_check_intersection_* functions

## Globals
- AXISLEN_EPSILON2 (const float): Minimum squared length for separating axis

## Dependencies
- colmath.h
- obbox.h
- tri.h
- wwdebug.h
- Vector3 class operations
- WWMath namespace functions
