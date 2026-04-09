# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/wwmathids.h - Enhanced Analysis

## Architectural Role
This header defines serialization chunk IDs for WWMath objects, serving as a critical bridge between the math library and the save/load system. It ensures unique identification of curve/spline types during game state persistence.

## Cross-References
### Incoming
- Save/load system (`saveloadids.h`) includes this for chunk ID definitions
- WWMath implementation files reference these IDs for serialization

### Outgoing
- None (header-only, no function calls)

## Design Patterns
- **Namespace via enum**: Uses anonymous enum to group related chunk IDs
- **Chunk ID allocation**: Follows `CHUNKID_WWMATH_BEGIN` pattern for hierarchical ID management
- **Serialization contract**: Defines the binary format interface for math objects

Key insight: The 0x100 offset between 1D and 3D curves suggests intentional grouping for version compatibility.
