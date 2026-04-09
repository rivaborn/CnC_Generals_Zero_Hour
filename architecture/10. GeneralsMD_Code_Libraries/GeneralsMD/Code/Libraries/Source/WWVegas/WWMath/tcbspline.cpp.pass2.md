# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tcbspline.cpp - Enhanced Analysis

## Architectural Role
This file implements TCB (Tension, Continuity, Bias) spline interpolation, extending the Hermite spline base class. It's part of the WWMath library, providing animation and pathfinding capabilities used by the W3D rendering system and game logic for smooth object movement.

## Cross-References
### Incoming
- Animation systems (likely in W3D or game logic) call `Add_Key`, `Update_Tangents`, and `Save/Load` for path interpolation.
- Persistence systems use `Get_Factory` for save/load registration.

### Outgoing
- Inherits from `HermiteSpline3DClass`, calling its methods for key management.
- Uses `Vector3` for 3D math operations.
- Relies on `ChunkSaveClass`/`ChunkLoadClass` for serialization.

## Design Patterns
- **Decorator Pattern**: Extends `HermiteSpline3DClass` with TCB-specific functionality while delegating base operations.
- **Factory Pattern**: Uses `SimplePersistFactoryClass` for object persistence registration.
- **Chunk-Based Serialization**: Implements save/load via chunked data streams for modular persistence.
