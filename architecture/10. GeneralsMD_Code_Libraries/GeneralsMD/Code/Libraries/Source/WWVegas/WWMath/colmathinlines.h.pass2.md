# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmathinlines.h - Enhanced Analysis

## Architectural Role
This header serves as a central hub for inline collision mathematics in the WWMath library, bridging core collision detection types (AABB, frustum, line, plane) used across rendering and AI subsystems.

## Cross-References
### Incoming
- `GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/*.cpp` (W3D rendering collision checks)
- `GeneralsMD/Code/Libraries/Source/Engine/AI/*.cpp` (pathfinding collision queries)
- `GeneralsMD/Code/Libraries/Source/Game/Unit/*.cpp` (unit collision detection)

### Outgoing
- Directly includes collision math type headers (`colmathaabox.h`, `colmathfrustum.h`, etc.)
- Indirectly depends on `WWMath` vector/matrix primitives

## Design Patterns
- **Header-Only Library**: Inline functions avoid linkage overhead for performance-critical collision math
- **Dependency Injection**: Collision types are passed as parameters rather than hardcoded
- **Modular Organization**: Separates collision math from rendering/AI logic while remaining accessible

*Not inferable*: No implementation details visible in header-only file.
