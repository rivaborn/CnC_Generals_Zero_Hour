# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmath.h - Enhanced Analysis

## Architectural Role
This header defines the core collision detection subsystem for the SAGE engine, providing geometric primitive classes and spatial relationship testing functions. It serves as the foundation for both physics simulation and visibility culling systems.

## Cross-References
### Incoming
- Physics system (for collision resolution)
- Rendering pipeline (for frustum culling)
- AI pathfinding (for obstacle detection)
- Projectile systems (for hit detection)

### Outgoing
- Uses `Vector3` for all spatial calculations
- Relies on `CastResultStruct` for collision details
- Depends on geometric primitive classes (AABox, OBBox, etc.)

## Design Patterns
- **Strategy Pattern**: Different collision tests are implemented as separate static methods, allowing the caller to choose the appropriate algorithm
- **Facade Pattern**: Provides a unified interface for complex collision detection operations
- **Singleton-like**: Uses static methods and global state for statistics tracking (though not a true singleton)
