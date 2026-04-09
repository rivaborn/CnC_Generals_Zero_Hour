# Generals/Code/Libraries/Source/WWVegas/WWMath/tcbspline.h - Enhanced Analysis

## Architectural Role
This file defines a specialized spline class for 3D interpolation, extending the Hermite spline base class. It's part of the WWMath library, providing mathematical utilities for the engine, particularly for animation and pathfinding systems.

## Cross-References
### Incoming
- Animation systems (e.g., unit movement, camera paths)
- Pathfinding/waypoint systems
- UI animation controllers

### Outgoing
- `HermiteSpline3DClass` (base class)
- `DynamicVectorClass` (container for TCB parameters)
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` (save/load infrastructure)

## Design Patterns
- **Inheritance**: Extends `HermiteSpline3DClass` to add TCB-specific functionality.
- **Encapsulation**: Bundles TCB parameters (`Tension`, `Continuity`, `Bias`) into a nested `TCBClass`.
- **Template Method**: Overrides virtual methods for key management and persistence.
