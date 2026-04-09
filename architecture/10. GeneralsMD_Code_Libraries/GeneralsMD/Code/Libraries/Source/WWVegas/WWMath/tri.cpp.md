# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tri.cpp

## Purpose
Implements triangle operations including dominant plane detection and point-in-triangle containment tests.

## Responsibilities
- Determines dominant plane axes for a triangle
- Performs 2D point-in-triangle tests
- Provides utility functions for triangle geometry

## Key Types
- **FDPRec (struct)**: Stores axis indices for dominant plane (axis1, axis2, axis3)
- **TriClass (Class)**: Main triangle class (defined elsewhere)

## Key Functions
### `find_dominant_plane_fast`
- Purpose: Quickly identifies dominant plane axes using triangle normal
- Calls: `WWMath::Fabs`

### `find_dominant_plane`
- Purpose: Determines dominant plane axes and returns them via pointers
- Calls: `WWMath::Fabs`

### `TriClass::Find_Dominant_Plane`
- Purpose: Member function to find dominant plane axes (2D version)
- Calls: `WWMath::Fabs`

### `TriClass::Contains_Point`
- Purpose: Tests if a point lies within a triangle using cross-product method
- Calls: `find_dominant_plane`, `Vector2::Set`, `WWMath::Fabs`

## Globals
- **dominance (FDPRec[3])**: Static lookup table for axis permutations

## Dependencies
- `tri.h` (header)
- `vector2.h` (Vector2 class)
- `WWMath::Fabs` (absolute value)
- `TriClass` (external class)
- `Vector3` (external class)
