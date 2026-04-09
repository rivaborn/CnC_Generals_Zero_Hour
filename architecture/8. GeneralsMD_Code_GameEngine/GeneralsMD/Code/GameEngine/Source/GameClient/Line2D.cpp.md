# GeneralsMD/Code/GameEngine/Source/GameClient/Line2D.cpp

## Purpose
Provides 2D geometric utility functions for line clipping, intersection, and point-in-region tests.

## Responsibilities
- Line clipping against rectangular regions
- Line intersection detection
- Point-in-rectangle/area containment tests
- Distance calculations between points and line segments

## Key Types
- None

## Key Functions
### ClipLine2D
- Purpose: Clips a line segment to a rectangular region
- Calls: None

### IntersectLine2D
- Purpose: Determines if two line segments intersect and finds intersection point
- Calls: None

### PointInsideRect2D
- Purpose: Tests if a point lies inside a rectangle defined by four corners
- Calls: ShortestDistancePointToSegment2D

### PointInsideArea2D
- Purpose: Uses even-odd winding rule to test if a point is inside a polygon
- Calls: IntersectLine2D

### ShortestDistancePointToSegment2D
- Purpose: Calculates shortest distance from point to line segment
- Calls: None

## Globals
- reallyFarPoint (Coord2D): A point far outside normal view for intersection tests

## Dependencies
- "Lib/BaseType.h" (for basic types)
- "GameClient/Line2D.h" (header)
- Coord2D, Coord3D, ICoord2D, IRegion2D (from BaseType.h)
