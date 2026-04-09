# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathline.h

## Purpose
Provides inline collision detection functions for line segments against axis-aligned bounding boxes.

## Responsibilities
- Defines collision test between line segments and AABBs
- Exposes `Overlap_Test` for line-box intersection
- Includes header guard for safety

## Key Types
- None

## Key Functions
### `Overlap_Test(const Vector3 &, const Vector3 &, const LineSegClass &)`
- Purpose: Tests overlap between a line segment and an AABB defined by min/max points.
- Calls: `AABoxClass::Init_Min_Max()`, `CollisionMath::Overlap_Test(AABoxClass, LineSegClass)`

## Globals
- None

## Dependencies
- `Vector3` (external)
- `LineSegClass` (external)
- `AABoxClass` (external)
- `CollisionMath` namespace (external)
