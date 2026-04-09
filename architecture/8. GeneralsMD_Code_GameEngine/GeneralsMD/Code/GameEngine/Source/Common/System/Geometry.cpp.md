# GeneralsMD/Code/GameEngine/Source/Common/System/Geometry.cpp

## Purpose
Implements geometry calculations and spatial queries for game objects.

## Responsibilities
- Provides geometry type parsing and configuration
- Calculates distances, intersections, and spatial relationships
- Manages bounding volumes (spheres, circles, boxes)
- Supports footprint operations (clipping, containment, random offsets)

## Key Types
- **GeometryInfo (Class)**: Stores and manages geometry parameters and calculations
- **GeometryType (Enum)**: Defines geometry types (sphere, cylinder, box)
- **Coord3D (Struct)**: 3D coordinate representation

## Key Functions
### calcDotProduct
- Purpose: Computes dot product of two 3D vectors
- Calls: None

### calcDistSquared
- Purpose: Calculates squared distance between two points
- Calls: None

### calcPointToLineDistSquared
- Purpose: Computes squared distance from point to line segment
- Calls: calcDotProduct, calcDistSquared

### isIntersectedByLineSegment
- Purpose: Checks if geometry is intersected by a line segment
- Calls: calcPointToLineDistSquared

### calcPitches
- Purpose: Calculates pitch angles between two geometries
- Calls: getCenterPosition, getMaxHeightAbovePosition, getMaxHeightBelowPosition

### get2DBounds
- Purpose: Computes 2D bounding region for rotated geometry
- Calls: None

### isPointInFootprint
- Purpose: Checks if point lies within geometry footprint
- Calls: isWithin

## Globals
- None

## Dependencies
- Common/Geometry.h
- Common/INI.h
- Common/RandomValue.h
- Common/Xfer.h
- PreRTS.h
- External: PI, sqr, clamp, GameLogicRandomValueReal, Cos, Sin
