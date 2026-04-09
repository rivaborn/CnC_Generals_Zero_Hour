# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/plane.h

## Purpose
Defines the `PlaneClass` for 3D plane operations using normal + distance representation.

## Responsibilities
- Plane initialization via multiple constructors
- Point/sphere plane intersection tests
- Plane-plane intersection calculations

## Key Types
- **PlaneClass (Class)**: Represents a 3D plane with normal vector and distance
- **FRONT/BACK/ON (Enum)**: Plane position relative to a point

## Key Functions
### PlaneClass(float nx,float ny,float nz,float dist)
- Purpose: Constructs plane from coefficients
- Calls: Set()

### Compute_Intersection(const Vector3 & p0,const Vector3 & p1,float * set_t)
- Purpose: Computes intersection between plane and line segment
- Calls: Vector3::Dot_Product()

### In_Front(const Vector3 & point)
- Purpose: Tests if point is in front of plane
- Calls: Vector3::Dot_Product()

### Intersect_Planes(const PlaneClass & a, const PlaneClass & b, Vector3 *line_dir, Vector3 *line_point)
- Purpose: Computes intersection line between two planes
- Calls: Vector3::Cross_Product(), Vector3::Normalize()

## Globals
None

## Dependencies
- `vector3.h` (Vector3 class)
- `sphere.h` (SphereClass)
- `always.h` (ALLOW_TEMPORARIES)
