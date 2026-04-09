# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tcbspline.h - Enhanced Analysis

## Architectural Role
This file implements a specialized spline class for 3D interpolation, extending the Hermite spline base class with TCB (Tension-Continuity-Bias) parameters. It's part of the WWMath library, providing mathematical utilities for the game engine, particularly for animation and pathfinding systems.

## Cross-References
### Incoming
- Animation systems (likely in W3D or game logic) that require smooth 3D interpolation
- Pathfinding components needing customizable spline behavior
- Save/load systems that persist spline data

### Outgoing
- `HermiteSpline3DClass` (base class for spline operations)
- `DynamicVectorClass` for parameter storage
- `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass` for serialization

## Design Patterns
- **Template Method**: The `Update_Tangents` method defines a hook for recalculating tangents based on TCB parameters, allowing derived classes to customize behavior.
- **Composite**: Uses `DynamicVectorClass<TCBClass>` to manage a collection of TCB parameters, treating them as a single unit.
- **Strategy**: TCB parameters act as a strategy for controlling spline interpolation, encapsulating different interpolation behaviors.
