# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/aabox.h

## Purpose
Defines axis-aligned bounding box (AABB) classes and related utilities for spatial calculations in 3D space.

## Responsibilities
- Provides AABoxClass for center-extent AABB representation
- Implements MinMaxAABoxClass for min/max corner AABB representation
- Supports transformations, containment tests, and spatial queries
- Includes utility functions for box initialization and expansion

## Key Types
- **AABoxClass (Class)**: Represents an axis-aligned box using center and extent vectors
- **MinMaxAABoxClass (Class)**: Represents an axis-aligned box using min/max corner points
- **Vector3 (Type)**: Used for 3D point/extent representation (external)
- **Matrix3D (Type)**: Used for transformations (external)

## Key Functions
### AABoxClass::Transform
- Purpose: Transforms the box to enclose its transformed version
- Calls: Matrix3D::Transform_Center_Extent_AABox

### AABoxClass::Add_Point
- Purpose: Expands the box to contain the given point
- Calls: None

### AABoxClass::Contains
- Purpose: Tests whether this box contains another box or point
- Calls: CollisionMath::Overlap_Test

### MinMaxAABoxClass::Transform
- Purpose: Updates the box to enclose its transformed version
- Calls: Matrix3D::Transform_Min_Max_AABox

### MinMaxAABoxClass::Add_Point
- Purpose: Updates the box to enclose the given point
- Calls: None

## Globals
None

## Dependencies
- "matrix3d.h" - Matrix3D class for transformations
- "lineseg.h" - LineSegClass for line segment operations
- "colmath.h" - CollisionMath for overlap tests
- Vector3 operations (external)
