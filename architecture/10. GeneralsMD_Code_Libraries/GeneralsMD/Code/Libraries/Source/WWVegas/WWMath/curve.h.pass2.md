# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/curve.h - Enhanced Analysis

## Architectural Role
This file defines the core curve interpolation system used across the engine for animation, movement, and other time-based value transitions. It provides a foundational abstraction for both 1D and 3D value interpolation, critical for game object behaviors and cinematic sequences.

## Cross-References
### Incoming
- `VehicleCurveClass` (from vehiclecurve.h) inherits from `Curve3DClass` and implements specialized arc-based movement curves
- Animation systems likely use these curves for keyframed animations
- Pathfinding/movement systems may use 3D curves for smooth transitions

### Outgoing
- Relies on `PersistClass` for save/load functionality
- Uses `Vector3` and `Vector` for mathematical operations
- Depends on `DynamicVectorClass` for key point storage

## Design Patterns
- **Template Method Pattern**: The base `Curve3DClass` and `Curve1DClass` define the interface for evaluation, with concrete implementations (e.g., `LinearCurve3DClass`) providing specific interpolation logic
- **Composite Pattern**: The `KeyClass` nested within curve classes forms a composite structure for managing multiple key points
- **Factory Pattern**: The `Get_Factory` method suggests integration with the engine's persistence factory system for object serialization

Rules followed. Output under 400 tokens.
