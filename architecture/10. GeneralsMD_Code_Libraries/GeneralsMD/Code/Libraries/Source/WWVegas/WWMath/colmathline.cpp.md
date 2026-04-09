# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathline.cpp

## Purpose
Implements collision detection between line segments and various geometric primitives (planes, triangles, spheres, axis-aligned boxes, and oriented bounding boxes).

## Responsibilities
- Line-segment collision tests with planes, triangles, spheres, and boxes
- Computes intersection points and normals
- Handles both axis-aligned and oriented bounding boxes
- Supports early-out checks for parallel rays

## Key Types
- **BoxTestStruct (struct)**: Holds intermediate data for box-line intersection tests
- **BoxSideType (enum)**: Categorizes point position relative to box axis projection (negative, middle, positive)
- **BOX_SIDE_NEGATIVE (enum)**: Negative side of box axis
- **BOX_SIDE_POSITIVE (enum)**: Positive side of box axis
- **BOX_SIDE_MIDDLE (enum)**: Middle region of box axis

## Key Functions
### Test_Aligned_Box
- Purpose: Core logic for testing line intersection with axis-aligned boxes
- Calls: None (inline helper)

### Collide (various overloads)
- Purpose: Public collision detection interface for different primitive types
- Calls: Test_Aligned_Box, Vector3 operations, plane/triangle/sphere methods

## Globals
- **_box_normal (Vector3[3][2])**: Precomputed normals for axis-aligned box faces

## Dependencies
- Key includes: `colmath.h`, `aaplane.h`, `plane.h`, `lineseg.h`, `tri.h`, `sphere.h`, `aabox.h`, `obbox.h`, `wwdebug.h`
- External symbols: `CollisionMath`, `Vector3`, `AAPlaneClass`, `PlaneClass`, `TriClass`, `SphereClass`, `AABoxClass`, `OBBoxClass`, `CastResultStruct`
