# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathline.h

## Purpose
Provides inline collision detection functions for line segments against axis-aligned bounding boxes.

## Responsibilities
- Defines line segment collision testing with AABB
- Exposes `Overlap_Test` for line-box intersection
- Includes header guard for safety

## Key Types
- `CollisionMath::OverlapType` (Enum): Result of collision test (Not inferable)
- `Vector3` (Struct): 3D point representation
- `LineSegClass` (Class): Line segment definition
- `AABoxClass` (Class): Axis-aligned bounding box

## Key Functions
### `CollisionMath::Overlap_Test(const Vector3&, const Vector3&, const LineSegClass&)`
- Purpose: Tests overlap between a line segment and an AABB defined by min/max points.
- Calls: `AABoxClass::Init_Min_Max()`, `CollisionMath::Overlap_Test(AABoxClass, LineSegClass)`

## Globals
- None

## Dependencies
- `CollisionMath` namespace (external)
- `Vector3`, `LineSegClass`, `AABoxClass` (external)
- `COLMATHLINE_H` (header guard)
