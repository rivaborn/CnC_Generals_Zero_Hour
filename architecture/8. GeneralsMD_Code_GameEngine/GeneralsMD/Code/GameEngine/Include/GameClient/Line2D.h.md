# GeneralsMD/Code/GameEngine/Include/GameClient/Line2D.h

## Purpose
Header file providing 2D line and geometry utility functions for collision detection, point-in-region checks, and line operations.

## Responsibilities
- Define 2D/3D coordinate vector types
- Declare line clipping and intersection functions
- Provide point-in-region containment tests
- Offer line-segment distance calculations
- Support rectangle scaling operations

## Key Types
- Coord2DVector (Class): Vector of 2D coordinates
- Coord3DVector (Class): Vector of 3D coordinates

## Key Functions
### ClipLine2D
- Purpose: Clip a line segment against a rectangular region
- Calls: Not inferable

### IntersectLine2D
- Purpose: Test if two line segments intersect and optionally return intersection point
- Calls: Not inferable

### PointInsideRect2D
- Purpose: Check if a 2D point lies inside a rectangle defined by four corners
- Calls: Not inferable

### Coord3DInsideRect2D
- Purpose: Check if a 3D point projects inside a 2D rectangle (ignoring Z)
- Calls: Not inferable

### ScaleRect2D
- Purpose: Scale a rectangle by a given factor
- Calls: Not inferable

### PointInsideRect3D
- Purpose: Check if a 3D point lies inside a 3D rectangle (ignoring Z)
- Calls: Not inferable

### PointInsideArea2D
- Purpose: Perform even-odd polygon containment test for 2D/3D points
- Calls: Not inferable

### ShortestDistancePointToSegment2D
- Purpose: Calculate shortest distance from point to line segment and optional intersection data
- Calls: Not inferable

## Globals
None
