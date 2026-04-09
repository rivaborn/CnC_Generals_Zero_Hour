# Generals/Code/GameEngine/Source/GameClient/Line2D.cpp

## Purpose
Provides utility functions for 2D line and point operations, including clipping, intersection, and containment tests.

## Responsibilities
- Line clipping and intersection calculations
- Point-in-rectangle and point-in-polygon tests
- Distance calculations between points and line segments
- Coordinate transformations and scaling

## Key Types
- None

## Key Functions
### ClipLine2D
- Purpose: Clips a line segment to a rectangular region.
- Calls: None

### IntersectLine2D
- Purpose: Determines if two line segments intersect and calculates intersection point.
- Calls: None

### PointInsideRect2D
- Purpose: Tests if a point lies inside a rectangle defined by four corners.
- Calls: ShortestDistancePointToSegment2D

### PointInsideArea2D
- Purpose: Uses even-odd winding rule to test if a point is inside a polygon.
- Calls: IntersectLine2D

### ShortestDistancePointToSegment2D
- Purpose: Calculates shortest distance from point to line segment and intersection point.
- Calls: None

## Globals
- reallyFarPoint (Coord2D): A point far outside typical screen coordinates used for ray casting.

## Dependencies
- "Lib/BaseType.h" - Base types and math utilities
- "GameClient/Line2D.h" - Header for this module
- Coord2D, Coord3D, ICoord2D, IRegion2D - Coordinate and region types
- Real, Int, Bool - Basic types
- sqr() - Math utility function
