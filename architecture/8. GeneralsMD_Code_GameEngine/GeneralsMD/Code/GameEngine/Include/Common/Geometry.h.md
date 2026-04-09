# GeneralsMD/Code/GameEngine/Include/Common/Geometry.h

## Purpose
Defines geometry types and the GeometryInfo class for spatial calculations in the game engine.

## Responsibilities
- Defines geometry types (sphere, cylinder, box)
- Provides GeometryInfo class for collision/partition testing
- Handles footprint calculations and spatial queries
- Supports serialization via Snapshot interface

## Key Types
- GeometryType (Enum): enumerates supported geometry types
- GeometryInfo (Class): encapsulates geometry properties and spatial operations

## Key Functions
### GeometryInfo::calcBoundingStuff
- Purpose: Calculates bounding circle/sphere radii
- Calls: None

### GeometryInfo::isIntersectedByLineSegment
- Purpose: Tests line segment intersection with geometry
- Calls: None

### GeometryInfo::getFootprintArea
- Purpose: Returns the 2D footprint area
- Calls: None

### GeometryInfo::calcPitches
- Purpose: Calculates pitch angles between two geometries
- Calls: None

## Globals
- GeometryNames[] (const char*): String representations of geometry types (conditionally defined)

## Dependencies
- BaseType.h, AsciiString.h, Snapshot.h
- INI class, Xfer class, Coord3D, Region2D
- Real type, Bool type
