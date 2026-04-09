# Generals/Code/Libraries/Source/WWVegas/WWMath/lineseg.h

## Purpose
Defines the LineSegClass for representing and manipulating 3D line segments.

## Responsibilities
- Store and manage line segment endpoints and derived properties
- Provide geometric operations (intersection, closest point)
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
### LineSegClass/LineSegClass (default constructor)
- Purpose: Default constructor
- Calls: None

### LineSegClass/LineSegClass (Vector3, Vector3)
- Purpose: Constructs line segment from two points
- Calls: recalculate()

### LineSegClass/Set (Vector3, Vector3)
- Purpose: Sets line segment endpoints
- Calls: recalculate()

### LineSegClass/Set (LineSegClass, Matrix3D)
- Purpose: Transforms line segment by matrix
- Calls: None

### LineSegClass/Set_Random (Vector3, Vector3)
- Purpose: Generates random line segment within bounds
- Calls: None

### LineSegClass/Find_Point_Closest_To (Vector3)
- Purpose: Finds closest point on segment to given position
- Calls: None

### LineSegClass/Find_Intersection (LineSegClass, Vector3*, float*, Vector3*, float*)
