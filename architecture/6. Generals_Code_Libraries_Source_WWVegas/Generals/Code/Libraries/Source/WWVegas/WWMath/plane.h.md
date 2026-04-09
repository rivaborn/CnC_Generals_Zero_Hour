# Generals/Code/Libraries/Source/WWVegas/WWMath/plane.h

## Purpose
Defines the `PlaneClass` for representing 3D planes using normal + distance.

## Responsibilities
- Represent 3D planes with normal and distance
- Provide plane initialization from various inputs
- Compute intersections and spatial relationships with points/spheres
- Calculate intersections between two planes

## Key Types
- **PlaneClass (Class)**: Represents a 3D plane with normal and distance
- **FRONT (Enum)**: Point is in front of plane
- **BACK (Enum)**: Point is behind plane
- **ON (Enum)**: Point is on plane

## Key Functions
### `PlaneClass(float nx, float ny, float nz, float dist)`
- Purpose: Constructs plane from coefficients
- Calls: `Set(float a, float b, float c, float d)`

### `PlaneClass(const Vector3 & normal, float dist)`
- Purpose: Constructs plane from normal and distance
- Calls: `Set(const Vector3 & normal, float dist)`

### `PlaneClass(const Vector3 & normal, const Vector3 & point)`
- Purpose: Constructs plane from normal containing a point
- Calls: `Set(const Vector3 & normal, const Vector3 & point)`

### `PlaneClass(const Vector3 & point1, const Vector3 & point2, const Vector3 & point3)`
- Purpose: Constructs plane from three points
- Calls: `Set(const Vector3 & point1, const Vector3 & point2, const Vector3 & point3)`

### `Compute_Intersection(const Vector3 & p0, const Vector3 & p1, float * set_t)`
- Purpose: Computes intersection of line segment with plane
- Calls: `Vector3::Dot_Product()`

### `In_Front(const Vector3 & point)`
- Purpose: Checks if point is in front of plane
- Calls: `Vector3::Dot_Product()`

### `In_Front(const SphereClass & sphere)`
- Purpose: Checks if sphere is entirely in front of plane
- Calls: `Vector3::Dot_Product()`

### `In_Front_Or_Intersecting(const SphereClass & sphere)`
- Purpose: Checks if sphere intersects or is in front of plane
- Calls: `Vector3::Dot_Product()`

### `Intersect_Planes(const PlaneClass & a, const PlaneClass & b, Vector3 *line_dir, Vector3 *line_point)`
- Purpose: Computes intersection line of two planes
- Calls: `Vector3::Cross_Product()`, `Vector3::Normalize()`

## Globals
None

## Dependencies
- `vector3.h` (Vector3 class)
- `sphere.h` (SphereClass)
- `always.h` (
