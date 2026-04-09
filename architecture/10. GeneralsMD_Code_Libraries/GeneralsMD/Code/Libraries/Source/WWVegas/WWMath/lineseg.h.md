# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/lineseg.h

## Purpose
Defines the `LineSegClass` for representing and manipulating 3D line segments.

## Responsibilities
- Store and manage line segment endpoints and derived properties
- Provide intersection and closest-point calculations
- Support transformations and random generation

## Key Types
- **LineSegClass (Class)**: Represents a 3D line segment with endpoints and derived properties
- **TriClass (Class)**: Forward declaration (not defined here)
- **AABoxClass (Class)**: Forward declaration (not defined here)
- **OBBoxClass (Class)**: Forward declaration (not defined here)
- **PlaneClass (Class)**: Forward declaration (not defined here)
- **SphereClass (Class)**: Forward declaration (not defined here)
- **Matrix3D (Class)**: Forward declaration (not defined here)

## Key Functions
### `LineSegClass(const Vector3 & p0, const Vector3 & p1)`
- Purpose: Constructs a line segment from two points
- Calls: `recalculate()`

### `Set(const Vector3 & p0, const Vector3 & p1)`
- Purpose: Updates the line segment endpoints
- Calls: `recalculate()`

### `Set(const LineSegClass & that, const Matrix3D & tm)`
- Purpose: Transforms a line segment using a matrix
- Calls: None visible

### `Find_Point_Closest_To(const Vector3 &pos)`
- Purpose: Finds the closest point on the segment to a given position
- Calls: None visible

### `Find_Intersection(const LineSegClass &other_line, Vector3 *p1, float *fraction1, Vector3 *p2, float *fraction2)`
- Purpose: Computes intersection with another line segment
- Calls: None visible

### `recalculate
