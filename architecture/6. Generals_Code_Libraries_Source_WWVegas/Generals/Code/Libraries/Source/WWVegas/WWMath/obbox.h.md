# Generals/Code/Libraries/Source/WWVegas/WWMath/obbox.h

## Purpose
Defines the `OBBoxClass` for oriented bounding box collision detection and manipulation.

## Responsibilities
- Represents oriented bounding boxes in 3D space
- Provides intersection and collision detection
- Supports transformations and projections
- Computes box properties (volume, extents)

## Key Types
- **OBBoxClass (Class)**: Oriented bounding box with center, extents, and basis (rotation)
- **TriClass (Class)**: Forward declaration (triangle class)
- **AABoxClass (Class)**: Forward declaration (axis-aligned box class)
- **PlaneClass (Class)**: Forward declaration (plane class)

## Key Functions
### `OBBoxClass::Project_To_Axis`
- Purpose: Computes projection of the box onto a given axis
- Calls: `Vector3::Dot_Product`, `WWMath::Fabs`

### `OBBoxClass::Transform`
- Purpose: Transforms an oriented box by a 3D matrix
- Calls: `Matrix3D::Transform_Vector`, `Matrix3::Multiply`

### `OBBoxClass::Compute_Point`
- Purpose: Computes world-space position of a parametric point in the box
- Calls: `Matrix3::Rotate_Vector`, `Vector3::Add`

### `OBBoxClass::Compute_Axis_Aligned_Extent`
- Purpose: Computes the axis-aligned extent enclosing this box
- Calls: `WWMath::Fabs`

### `Oriented_Boxes_Intersect`
- Purpose: Tests if two oriented boxes intersect
- Calls: Not inferable (external function)

### `Oriented_Boxes_Collide`
- Purpose: Tests if two moving oriented boxes collide within a time step
- Calls: Not inferable (external function)

### `Oriented_Box_Intersects_Tri`
- Purpose: Tests if an oriented box intersects a triangle
- Calls: Not inferable (external function)

## Globals
None

## Dependencies
- `vector3.h`, `matrix3.h`, `matrix3d.h`, `wwmath.h`, `castres.h`
- `TriClass`, `AABoxClass`, `PlaneClass` (forward declarations)
