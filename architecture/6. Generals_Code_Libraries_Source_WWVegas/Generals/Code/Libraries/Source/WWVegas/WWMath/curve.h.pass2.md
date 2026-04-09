# Generals/Code/Libraries/Source/WWVegas/WWMath/curve.h - Enhanced Analysis

## Architectural Role
This file defines the core curve interpolation system used across the engine for animation, movement, and procedural generation. It serves as a foundational math utility for both 1D and 3D value interpolation, with persistence support for save/load functionality.

## Cross-References
### Incoming
- `VehicleCurveClass` (from `vehiclecurve.h`) inherits from `Curve3DClass` and uses its evaluation system
- Animation systems likely use `Curve1DClass` for property interpolation
- Game object movement systems may use `Curve3DClass` for pathfinding/waypoint interpolation

### Outgoing
- Uses `PersistClass` for save/load functionality
- Relies on `Vector3` and `Vector` for mathematical operations
- Uses `DynamicVectorClass` for key point storage

## Design Patterns
- **Template Method Pattern**: Base curve classes define evaluation interface while derived classes implement specific interpolation logic
- **Composite Pattern**: Key points are stored in a dynamic vector, allowing for flexible curve construction
- **Persistence Pattern**: Implements save/load through `ChunkLoadClass`/`ChunkSaveClass` for game state serialization

*Not inferable*: Specific usage patterns in animation or AI systems would require examining calling code.
