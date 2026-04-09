# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/hermitespline.cpp - Enhanced Analysis

## Architectural Role
This file implements Hermite spline interpolation, a core mathematical utility used for smooth motion paths in the game. It bridges the WWMath library with the game's animation and pathfinding systems, providing both 1D and 3D spline evaluation capabilities.

## Cross-References
### Incoming
- Animation systems (likely in W3D) use `Evaluate` for interpolating object positions
- Pathfinding/AI subsystems call `Evaluate_Derivative` for velocity calculations
- Save/load systems reference the persistence factories

### Outgoing
- Calls into `Curve3DClass`/`Curve1DClass` base implementations
- Uses `PersistFactoryClass` for serialization
- Relies on `Vector3` for 3D math operations

## Design Patterns
- **Template Method**: Base curve classes define save/load interface, derived classes implement specifics
- **Lazy Evaluation**: Tangents recomputed only when dirty flag is set
- **Composite**: Spline keys and tangents stored as separate arrays managed together

*Not inferable*: Exact usage patterns in animation/pathfinding systems.
