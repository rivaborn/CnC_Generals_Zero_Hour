# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathobbobb.cpp

## Purpose
Implements collision detection between oriented bounding boxes (OBBs) and axis-aligned bounding boxes (AABBs) using separating axis theorem.

## Responsibilities
- Tests intersection between two OBBs
- Computes collision contact points and normals
- Handles OBB-AABB and AABB-OBB collision cases
- Implements separating axis tests for 15 potential axes
- Provides optimized projection calculations

## Key Types
- ObbIntersectionStruct (Class): Holds intermediate data for OBB intersection tests
- ObbCollisionStruct (Class): Holds intermediate data for OBB collision tests
- (anonymous enum) (Enum): Defines axis types for collision tests

## Key Functions
### intersect_obb_obb
- Purpose: Tests if two OBBs intersect
- Calls: obb_intersect_box0_basis, obb_intersect_box1_basis, obb_intersect_axis

### collide_obb_obb
- Purpose: Tests collision between two moving OBBs and computes contact info
- Calls: obb_check_box0_basis, obb_check_box1_basis, obb_check_axis, obb_compute_projections, compute_contact_normal, compute_contact_point

### compute_contact_normal
- Purpose: Calculates the contact normal after collision detection
- Calls: Vector3::Cross_Product, Vector3::Dot_Product

### compute_contact_point
- Purpose: Computes the exact contact point between colliding OBBs
- Calls: Vector3::Dot_Product, Vector3::Add

## Globals
- AXISLEN_EPSILON2 (float): Minimum squared length for separating axis

## Dependencies
- colmath.h
- obbox.h
- aabox.h
- wwdebug.h
- Vector3 class methods
- WWMath namespace functions
