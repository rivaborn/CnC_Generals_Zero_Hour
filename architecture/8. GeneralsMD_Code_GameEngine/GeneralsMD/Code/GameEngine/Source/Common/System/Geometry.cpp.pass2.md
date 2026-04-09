# GeneralsMD/Code/GameEngine/Source/Common/System/Geometry.cpp - Enhanced Analysis

## Architectural Role
This file serves as the core spatial computation library for the SAGE engine, providing essential geometric primitives used across game logic, collision detection, and pathfinding. Its functions are fundamental to both runtime calculations (e.g., unit positioning) and editor tools (e.g., footprint visualization).

## Cross-References
### Incoming
- **Game Logic**: Unit/Building movement systems use `calcDistSquared` and `isPointInFootprint` for collision and placement validation
- **AI**: Pathfinding and tactical positioning rely on `get2DBounds` and `calcPitches` for spatial queries
- **W3D Rendering**: Uses `isIntersectedByLineSegment` for frustum culling and occlusion tests
- **UI**: Footprint visualization tools call `get2DBounds` for selection highlighting

### Outgoing
- **Common/INI.h**: For configuration parsing of geometry parameters
- **Common/RandomValue.h**: For procedural geometry generation (e.g., random offsets)
- **Common/Xfer.h**: For serialization in save/load and networking

## Design Patterns
- **Data-Oriented Design**: Geometry parameters are stored in a flat `GeometryInfo` struct with calculated derived values (e.g., bounding radii) to optimize cache locality
- **Strategy Pattern**: Geometry type-specific calculations are dispatched via `switch` statements on `m_type`, allowing extension to new geometry types without modifying callers
- **Lazy Calculation**: Bounding volumes are recalculated only when parameters change (via `calcBoundingStuff()`), not on every query

*Not inferable*: No clear use of Observer or Factory patterns in this file.
