# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathline.cpp

## Purpose
Implements collision detection between line segments and various geometric primitives (planes, triangles, spheres, axis-aligned boxes, and oriented bounding boxes).

## Responsibilities
- Line-segment collision tests with planes, triangles, spheres, and boxes
- Computes intersection points and normals for collisions
- Handles both axis-aligned and oriented bounding boxes
- Supports early-out checks for parallel rays

## Key Types
- **BoxTestStruct (Class)**: Holds intermediate data for box-line intersection tests
- **BoxSideType (Enum)**: Categorizes point position relative to box axis (negative/positive/middle)
- **BOX_SIDE_NEGATIVE (Enum)**: Negative side of box axis
- **BOX_SIDE_POSITIVE (Enum)**: Positive side of box axis
- **BOX_SIDE_MIDDLE (Enum)**: Point lies within box bounds on this axis

## Key Functions
### Test_Aligned_Box
- Purpose: Core logic for axis-aligned box-line intersection test
- Calls: None (inline helper)

### Collide (LineSegClass, AAPlaneClass)
- Purpose: Tests line-segment vs. axis-aligned plane collision
- Calls: None

### Collide (LineSegClass, PlaneClass)
- Purpose: Tests line-segment vs. arbitrary plane collision
- Calls: None

### Collide (LineSegClass, TriClass)
- Purpose: Tests line-segment vs. triangle collision
- Calls: TriClass::Contains_Point

### Collide (LineSegClass, SphereClass)
- Purpose: Tests line-segment vs. sphere collision
- Calls: WWMath::Sqrt

### Collide (LineSegClass, AABoxClass)
- Purpose: Tests line-segment vs. axis-aligned box collision
- Calls: Test_Aligned_Box

### Collide (LineSegClass, OBBoxClass)
- Purpose: Tests line-segment vs. oriented bounding box collision
- Calls: Test_Aligned_Box

## Globals
- **_box_normal (Vector3[3][2])**: Precomputed normals for axis-aligned box faces

## Dependencies
- Key includes: colmath.h, aaplane.h, plane.h, lineseg.h, tri.h, sphere.h, aabox.h, obbox.h, wwdebug.h
- External symbols: Vector3, CollisionMath, CastResultStruct, AAPlaneClass, PlaneClass, TriClass, SphereClass, AABoxClass, OBBoxClass, WWMath
