# Generals/Code/Libraries/Source/WWVegas/WWMath/tcbspline.cpp - Enhanced Analysis

## Architectural Role
This file implements TCB (Tension, Continuity, Bias) spline interpolation, extending the Hermite spline base class. It's part of the WWMath library, providing animation and pathfinding capabilities used by the W3D rendering system and game logic for smooth object movement.

## Cross-References
### Incoming
- Animation systems (e.g., unit movement, camera paths)
- W3D model interpolation
- Save/load game state (via persistfactory)

### Outgoing
- HermiteSpline3DClass (base class)
- Vector3 (math operations)
- ChunkSaveClass/ChunkLoadClass (serialization)

## Design Patterns
- **Decorator Pattern**: Extends HermiteSpline3DClass with TCB-specific behavior while reusing base functionality.
- **Factory Pattern**: Uses SimplePersistFactoryClass for object persistence.
- **Data-Driven Design**: TCB parameters (tension/continuity/bias) are configurable per-key, enabling runtime behavior modification.

*Not inferable*: No clear use of Observer or Strategy patterns despite interpolation flexibility.
