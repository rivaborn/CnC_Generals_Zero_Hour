# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathobbtri.cpp

## Purpose
Implements collision detection between oriented bounding boxes (OBBox) and triangles, including both intersection tests and collision response calculations.

## Responsibilities
- Tests for separation between OBBox and triangle using separating axis theorem
- Computes collision contact points and normals
- Performs intersection tests between OBBox and triangle
- Handles both static and dynamic collision scenarios

## Key Types
- BTCollisionStruct (Class): Context structure for OBBox-triangle collision detection
- BTIntersectStruct (Class): Context structure for OBBox-triangle intersection tests
- (anonymous enum) (Enum): Defines axis types for collision tests (INTERSECTION, AXIS_N, AXIS_A0, etc.)

## Key Functions
### obbtri_collision_separation_test
- Purpose: Tests if objects are separated along a given axis
- Calls: None

### obbtri_check_collision_axis
- Purpose: Projects OBBox and triangle onto arbitrary axis and tests for separation
- Calls: obbtri_collision_separation_test, Vector3::Dot_Product, Vector3::Length

### obbtri_compute_contact_normal
- Purpose: Computes the normal vector for a collision
- Calls: Vector3::Cross_Product, Vector3::Dot_Product

### obbtri_compute_contact_point
- Purpose: Calculates the contact point between OBBox and triangle
- Calls: eval_A0_point, eval_A1_point, eval_A2_point, Vector3::Dot_Product

### CollisionMath::Intersection_Test
- Purpose: Tests if OBBox intersects with triangle
- Calls: obbtri_check_intersection_normal_axis, obbtri_check_intersection_basis_axis, obbtri_check_intersection_cross_axis

## Globals
- AXISLEN_EPSILON2 (const float): Minimum squared length for separating axis

## Dependencies
- colmath.h
- obbox.h
- tri.h
- wwdebug.h
- Vector3 class operations
- WWMath namespace functions
