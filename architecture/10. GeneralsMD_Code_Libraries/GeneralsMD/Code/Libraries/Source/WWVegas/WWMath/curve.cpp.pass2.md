# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/curve.cpp - Enhanced Analysis

## Architectural Role
This file implements the core curve interpolation system used throughout the engine for animation, movement, and other time-based value transitions. It provides both 1D and 3D curve classes with persistence support, serving as a foundational math utility for other subsystems.

## Cross-References
### Incoming
- `vehiclecurve.cpp` uses `Evaluate`, `Find_Tangent`, `Find_Tangents`, `Find_Turn_Arc`, `Get_Angle_Delta`, and `Update_Arc_List` (likely for vehicle pathfinding/navigation)

### Outgoing
- Uses `ChunkSaveClass` and `ChunkLoadClass` for persistence
- Relies on `Vector3` for 3D point representation
- Uses `SimplePersistFactoryClass` for serialization

## Design Patterns
- **Template Method Pattern**: Base curve classes define interface for evaluation while derived classes implement specific interpolation logic
- **Composite Pattern**: Curve classes manage collections of key points
- **Factory Pattern**: Uses `SimplePersistFactoryClass` for object serialization/deserialization

*Not inferable*: Specific usage patterns in game logic (e.g., animation curves vs. pathfinding) would require examining callers.
