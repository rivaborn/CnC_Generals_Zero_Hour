# Generals/Code/Libraries/Source/WWVegas/WWMath/colmathaabox.h

## Purpose
Provides collision detection functions for axis-aligned bounding boxes (AABoxes) in 3D space.

## Responsibilities
- Tests overlap between an AABox and a point
- Tests overlap between two AABoxes
- Determines containment relationships between AABoxes

## Key Types
- `CollisionMath::OverlapType` (enum): Result of overlap tests (NEG, POS, BOTH)

## Key Functions
### `CollisionMath::Overlap_Test(const AABoxClass &, const Vector3 &)`
- Purpose: Tests if a point overlaps with an AABox.
- Calls: `WWMath::Fabs`

### `CollisionMath::Overlap_Test(const AABoxClass &, const AABoxClass &)`
- Purpose: Tests overlap/containment between two AABoxes.
- Calls: `Vector3::Subtract`, `WWMath::Fabs`

## Globals
None

## Dependencies
- `always.h`, `aabox.h`, `vector3.h`, `lineseg.h`
- `WWMath::Fabs`, `Vector3::Subtract`
