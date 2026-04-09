# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/tri.h - Enhanced Analysis

## Architectural Role
This file provides core geometric primitives for collision detection, bridging the WWMath library with the SAGE engine's rendering and physics systems. It encapsulates triangle operations used across multiple subsystems, particularly for terrain and object interaction.

## Cross-References
### Incoming
- **Physics/Collision System**: Uses `Cast_Semi_Infinite_Axis_Aligned_Ray_To_Triangle` for raycasting against terrain and objects
- **Render Objects**: Likely called by terrain rendering code for normal computation and point containment tests
- **AI Pathfinding**: May use `Point_In_Triangle_2D` for navigation mesh queries

### Outgoing
- **WWMath Vector Classes**: Heavily depends on `Vector2`, `Vector3`, and `Vector4` for all geometric operations
- **Assert System**: Uses `always.h` for runtime validation of triangle state

## Design Patterns
- **Data-Oriented Design**: `TriClass` uses raw pointers to vertices/normal for cache efficiency in collision checks
- **Utility Function Pattern**: Standalone functions like `Point_In_Triangle_2D` are designed for reuse across subsystems
- **Inline Optimization**: Critical functions are marked `inline` to avoid call overhead in hot collision paths

*Not inferable: No clear use of object-oriented patterns beyond basic class structure.*
