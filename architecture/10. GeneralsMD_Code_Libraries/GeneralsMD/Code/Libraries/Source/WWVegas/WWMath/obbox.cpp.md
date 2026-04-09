# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/obbox.cpp

## Purpose
Implements oriented bounding box (OBBox) collision detection and intersection tests.

## Responsibilities
- Provides OBBox construction from points or random initialization
- Implements intersection/collision tests between two OBBoxes
- Implements intersection tests between OBBox and triangle
- Uses Separating Axis Theorem (SAT) for collision detection

## Key Types
- OBBoxClass (Class): Represents an oriented bounding box with center, basis, and extent
- Vector3 (Struct): 3D vector math operations
- TriClass (Class): Triangle geometry representation

## Key Functions
### Oriented_Boxes_Intersect_On_Axis
- Purpose: Tests if two boxes intersect on a given axis
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Oriented_Boxes_Intersect
- Purpose: Tests if two oriented boxes intersect using SAT
- Calls: Oriented_Boxes_Intersect_On_Axis, Vector3::Cross_Product

### Oriented_Boxes_Collide_On_Axis
- Purpose: Tests if two moving boxes collide on a given axis
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Oriented_Boxes_Collide
- Purpose: Tests if two moving oriented boxes collide using SAT
- Calls: Oriented_Boxes_Collide_On_Axis, Vector3::Cross_Product

### Oriented_Box_Intersects_Tri_On_Axis
- Purpose: Tests if box and triangle intersect on a given axis
- Calls: Vector3::Dot_Product, WWMath::Fabs

### Oriented_Box_Intersects_Tri
- Purpose: Tests if oriented box intersects a triangle using SAT
- Calls: Oriented_Box_Intersects_Tri_On_Axis, Vector3::Cross_Product

## Globals
None

## Dependencies
- obbox.h, matrix3.h, vector3.h, aabox.h, tri.h, plane.h, quat.h
- WWMath namespace functions (Fabs, Random_Float)
- Vector3 class methods (Cross_Product, Dot_Product, Length2, etc.)
