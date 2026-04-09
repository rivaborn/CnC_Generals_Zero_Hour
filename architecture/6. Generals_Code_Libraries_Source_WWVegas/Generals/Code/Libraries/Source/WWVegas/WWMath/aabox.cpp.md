# Generals/Code/Libraries/Source/WWVegas/WWMath/aabox.cpp

## Purpose
Implements axis-aligned bounding box (AABB) functionality for collision detection and spatial queries.

## Responsibilities
- Initializes AABBs with random or empty states
- Tests containment of points and other AABBs
- Transforms AABBs via matrix operations

## Key Types
- AABoxClass (Class): Represents an axis-aligned bounding box with center and extent
- MinMaxAABoxClass (Class): Represents an AABB defined by min/max corners

## Key Functions
### AABoxClass::Init_Random
- Purpose: Initializes an AABB with random center and extent values
- Calls: WWMath::Random_Float()

### AABoxClass::Transform
- Purpose: Transforms an input AABB by a matrix and stores result in output
- Calls: Matrix3D::Transform_Center_Extent_AABox()

### MinMaxAABoxClass::Init_Empty
- Purpose: Initializes a min/max AABB to an empty state (infinite bounds)
- Calls: None

## Globals
None

## Dependencies
- aabox.h (header)
- colmath.h (collision math utilities)
- colmathinlines.h (inline collision math)
- float.h (for FLT_MAX constant)
