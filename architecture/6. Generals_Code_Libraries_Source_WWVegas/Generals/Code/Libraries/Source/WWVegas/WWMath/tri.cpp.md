# Generals/Code/Libraries/Source/WWVegas/WWMath/tri.cpp

## Purpose
Implements triangle operations including dominant plane detection and point-in-triangle containment tests.

## Responsibilities
- Determines dominant plane axes for a triangle
- Performs 2D point-in-triangle tests
- Provides utility functions for triangle analysis

## Key Types
- **FDPRec (struct)**: Stores axis indices for dominant plane (axis1, axis2, axis3)
- **TriClass (class)**: Main triangle class (defined elsewhere)

## Key Functions
### find_dominant_plane_fast
- Purpose: Quickly identifies dominant plane axes using a lookup table
- Calls: WWMath::Fabs

### find_dominant_plane
- Purpose: Determines dominant plane axes by comparing normal components
- Calls: WWMath::Fabs

### TriClass::Find_Dominant_Plane
- Purpose: Returns indices of two perpendicular axes for the dominant plane
- Calls: WWMath::Fabs

### TriClass::Contains_Point
- Purpose: Tests if a point lies within a triangle using cross-product method
- Calls: find_dominant_plane, Vector2 operations

## Globals
- **dominance (const FDPRec[3])**: Lookup table mapping dominant axes to perpendicular axes

## Dependencies
- tri.h (header)
- vector2.h (Vector2 class)
- WWMath namespace (Fabs function)
