# Generals/Code/Libraries/Source/WWVegas/WWMath/aabox.h

## Purpose
Defines axis-aligned bounding box (AABB) classes and related functionality for spatial queries and collision detection.

## Responsibilities
- Provides AABoxClass for center-extent AABBs
- Implements MinMaxAABoxClass for min-max corner representation
- Supports box initialization, transformation, and containment tests
- Includes utility functions for box operations

## Key Types
- **AABoxClass (Class)**: Center-extent axis-aligned bounding box
- **MinMaxAABoxClass (Class)**: Min-max corner axis-aligned bounding box
- **Vector3 (Type)**: 3D vector used for positions and extents

## Key Functions
### AABoxClass::Transform
- Purpose: Transforms the box to enclose its transformed form
- Calls: Matrix3D::Transform_Center_Extent_AABox

### AABoxClass::Add_Point
- Purpose: Expands the box to contain a given point
- Calls: None

### AABoxClass::Contains
- Purpose: Tests if the box contains another box or point
- Calls: CollisionMath::Overlap_Test

### MinMaxAABoxClass::Transform
- Purpose: Updates the box to enclose its transformed version
- Calls: Matrix3D::Transform_Min_Max_AABox

## Globals
None

## Dependencies
- matrix3d.h
- lineseg.h
- colmath.h
- always.h
- Vector3, Matrix3D, LineSegClass, CollisionMath
