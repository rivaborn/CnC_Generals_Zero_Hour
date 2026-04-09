# Generals/Code/Libraries/Source/WWVegas/WWMath/obbox.cpp

## Purpose
Implements oriented bounding box (OBBox) collision detection and intersection tests.

## Responsibilities
- Provides OBBox construction methods
- Implements OBBox-OBBox intersection/collision tests
- Implements OBBox-triangle intersection tests
- Handles both static and dynamic (velocity-based) collision checks

## Key Types
- OBBoxClass: Oriented bounding box with center, basis, and extent
- Vector3: 3D vector math operations
- TriClass: Triangle geometry representation

## Key Functions
### Oriented_Boxes_Intersect_On_Axis
- Purpose: Tests if two OBBoxes intersect along a given axis
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Oriented_Boxes_Intersect
- Purpose: Tests if two OBBoxes intersect using separating axis test
- Calls: Oriented_Boxes_Intersect_On_Axis, Vector3::Cross_Product

### Oriented_Boxes_Collide_On_Axis
- Purpose: Tests if two moving OBBoxes will collide along a given axis
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Oriented_Boxes_Collide
- Purpose: Tests if two moving OBBoxes will collide using separating axis test
- Calls: Oriented_Boxes_Collide_On_Axis, Vector3::Cross_Product

### Oriented_Box_Intersects_Tri_On_Axis
- Purpose: Tests if an OBBox and triangle intersect along a given axis
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Oriented_Box_Intersects_Tri
- Purpose: Tests if an OBBox and triangle intersect using separating axis test
- Calls: Oriented_Box_Intersects_Tri_On_Axis, Vector3::Cross_Product

## Globals
None

## Dependencies
- obbox.h, matrix3.h, vector3.h, aabox.h, tri.h, plane.h, quat.h
- WWMath namespace functions (Fabs, Random_Float)
- Vector3 class methods (Cross_Product, Dot_Product, Length2, etc.)
