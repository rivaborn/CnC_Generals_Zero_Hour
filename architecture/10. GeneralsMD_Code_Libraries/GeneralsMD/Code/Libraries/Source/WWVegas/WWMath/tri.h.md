# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tri.h

## Purpose
Provides triangle-related mathematical utilities for collision detection and geometric operations in the SAGE engine.

## Responsibilities
- Defines `TriClass` for triangle representation and operations
- Implements 2D point-in-triangle tests
- Handles semi-infinite axis-aligned ray-triangle intersection tests
- Computes triangle normals and plane dominance

## Key Types
- **TriClass (Class)**: Represents a triangle with three vertices and a normal vector
- **Anonymous Enum**: Flags for raycasting results (edge hit, start in triangle)
- **TRI_RAYCAST_FLAG_* (Enum values)**: Bitmask flags for raycasting

## Key Functions
### `Point_In_Triangle_2D`
- Purpose: Tests if a point lies inside a 2D triangle projection
- Calls: `Vector2::Perp_Dot_Product`, `Vector2::Length2`

### `Cast_Semi_Infinite_Axis_Aligned_Ray_To_Triangle`
- Purpose: Tests intersection between a semi-infinite axis-aligned ray and a triangle
- Calls: `Point_In_Triangle_2D`, `TriClass::Contains_Point`

### `TriClass::Compute_Normal`
- Purpose: Computes the triangle's normal vector via cross product
- Calls: `Vector3::Cross_Product`, `Vector3::Normalize`

### `TriClass::Contains_Point`
- Purpose: Checks if a point lies inside the triangle (3D)
- Calls: Not inferable (declared but not defined in this file)

### `TriClass::Find_Dominant_Plane`
- Purpose: Determines the dominant plane axes for the triangle
- Calls: Not inferable (declared but not defined in this file)

## Globals
- **sign (const float[2])**: Helper array for ray direction sign conversion

## Dependencies
- `vector4.h`, `vector3.h`, `vector2.h` (vector math)
- `always.h` (assert macros)
- `assert.h` (debug assertions)
