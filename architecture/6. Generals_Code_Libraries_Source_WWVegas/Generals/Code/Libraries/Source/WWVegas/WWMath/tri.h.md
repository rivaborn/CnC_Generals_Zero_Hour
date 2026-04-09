# Generals/Code/Libraries/Source/WWVegas/WWMath/tri.h

## Purpose
Provides triangle-related mathematical utilities for collision detection and geometric operations.

## Responsibilities
- Triangle point containment tests
- Ray-triangle intersection calculations
- Triangle normal computation
- Degenerate triangle handling

## Key Types
- **TriClass (Class)**: Represents a triangle with three vertices and a normal vector.
- **Anonymous Enum**: Flags for raycasting results (edge hit, start in triangle).
- **TRI_RAYCAST_FLAG_* (Enum values)**: Bitmask flags for raycasting.

## Key Functions
### Point_In_Triangle_2D
- Purpose: Tests if a point lies inside a 2D triangle projection.
- Calls: Vector2::Perp_Dot_Product, Vector2::Length2

### Cast_Semi_Infinite_Axis_Aligned_Ray_To_Triangle
- Purpose: Tests intersection between a semi-infinite axis-aligned ray and a triangle.
- Calls: Point_In_Triangle_2D, TriClass::Contains_Point

### TriClass::Compute_Normal
- Purpose: Computes the normal vector for the triangle.
- Calls: Vector3::Cross_Product, Vector3::Normalize

### TriClass::Contains_Point
- Purpose: Checks if a point is inside the triangle (forward declaration only).

### TriClass::Find_Dominant_Plane
- Purpose: Determines the dominant plane axes for the triangle (forward declaration only).

## Globals
- **sign (const float[2])**: Helper array for ray direction sign conversion.

## Dependencies
- "vector4.h", "vector3.h", "vector2.h", "always.h"
- Vector3, Vector2, Vector4 classes
- Vector3::Cross_Product, Vector3::Normalize
- Vector2::Perp_Dot_Product, Vector2::Length2
