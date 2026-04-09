# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/obbox.h

## Purpose
Defines the `OBBoxClass` for oriented bounding box collision detection and manipulation.

## Responsibilities
- Represents 3D oriented bounding boxes with center, extents, and basis (rotation).
- Provides intersection/collision tests between boxes and triangles.
- Supports transformations, projections, and point computations.

## Key Types
- **OBBoxClass (Class)**: Oriented bounding box with center, extents, and basis.
- **TriClass (Class)**: Forward declaration (triangle).
- **AABoxClass (Class)**: Forward declaration (axis-aligned box).
- **PlaneClass (Class)**: Forward declaration (plane).

## Key Functions
### `Oriented_Boxes_Intersect`
- Purpose: Tests if two oriented boxes intersect.
- Calls: Not inferable.

### `Oriented_Boxes_Collide`
- Purpose: Tests collision between two moving oriented boxes.
- Calls: Not inferable.

### `Oriented_Box_Intersects_Tri`
- Purpose: Tests if an oriented box intersects a triangle.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `vector3.h`, `matrix3.h`, `matrix3d.h`, `wwmath.h`, `castres.h`
- `TriClass`, `AABoxClass`, `PlaneClass` (forward declarations)
