# Generals/Code/Libraries/Source/WWVegas/WWMath/hermitespline.cpp - Enhanced Analysis

## Architectural Role
This file implements Hermite spline interpolation, a core mathematical utility used for smooth motion paths in the game. It bridges the WWMath library with the broader engine, particularly for animation and pathfinding systems.

## Cross-References
### Incoming
- Animation systems (e.g., unit movement, camera paths)
- Pathfinding/waypoint logic
- Save/load serialization (via `PersistFactoryClass`)

### Outgoing
- `Curve3DClass`/`Curve1DClass` (base curve implementations)
- `PersistFactoryClass` (for save/load)
- `Vector3` (for 3D point operations)

## Design Patterns
- **Lazy Evaluation**: Tangents are recomputed only when dirty (`TangentsDirty` flag).
- **Composite Pattern**: `HermiteSpline3DClass` extends `Curve3DClass`, inheriting key management while adding Hermite-specific behavior.
- **Factory Pattern**: Uses `SimplePersistFactoryClass` for serialization, enabling modular save/load.

*Not inferable*: Exact callers (e.g., animation systems) not visible in this file.
