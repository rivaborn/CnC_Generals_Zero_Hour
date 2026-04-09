# Generals/Code/Tools/WW3D/pluglib/plane.h

## Purpose
Defines a 3D plane class and utility functions for geometric calculations in the SAGE engine.

## Responsibilities
- Represents 3D planes with normal vector and distance
- Provides constructors for various plane creation methods
- Implements point-plane relationship testing
- Handles edge cases like colinear points

## Key Types
- **PlaneClass (Class)**: Represents a 3D plane defined by normal vector and distance
- **Vector3 (Class)**: Used for 3D vector operations (external)

## Key Functions
### `In_Front`
- Purpose: Tests if a point is in front of a plane
- Calls: `Vector3` dot product operator

## Globals
- None

## Dependencies
- `vector3.h` (Vector3 class)
- Uses Vector3 operations (Dot_Product, Cross_Product, Normalize)
