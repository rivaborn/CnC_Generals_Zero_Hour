# GeneralsMD/Code/GameEngine/Include/Common/Geometry.h - Enhanced Analysis

## Architectural Role
This file defines the core spatial abstraction layer for the SAGE engine, bridging physics, collision, and partitioning systems. GeometryInfo acts as a lightweight, serializable wrapper for collision volumes, used extensively by game objects for spatial queries and partition management.

## Cross-References
### Incoming
- Partition manager (depends on GeometryType ordering)
- Collision system (uses GeometryInfo for intersection tests)
- Game object classes (use GeometryInfo for spatial properties)
- INI parsing system (calls parseGeometry* methods)

### Outgoing
- Snapshot system (inherits for serialization)
- Math utilities (uses Coord3D, Region2D)
- Random number generation (for footprint offsets)

## Design Patterns
- **Data Transfer Object**: GeometryInfo encapsulates geometry data for serialization/deserialization
- **Strategy Pattern**: GeometryType enum enables polymorphic behavior for different collision shapes
- **Facade**: Hides complex spatial calculations behind simple interface methods

*Not inferable*: Exact usage of calcBoundingStuff in partition manager not visible.
