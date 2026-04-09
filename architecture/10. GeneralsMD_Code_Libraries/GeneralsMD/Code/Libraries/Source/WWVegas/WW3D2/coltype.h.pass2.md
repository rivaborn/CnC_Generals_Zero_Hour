# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/coltype.h - Enhanced Analysis

## Architectural Role
This header defines the collision type bit-field system used by the W3D rendering subsystem for spatial queries. It enables selective collision detection between different object types (e.g., physical bodies vs. projectiles) by providing a low-level masking mechanism.

## Cross-References
### Incoming
- `GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/*.cpp` (W3D rendering code)
- `GeneralsMD/Code/Game/Logic/*.cpp` (game logic collision checks)
- `GeneralsMD/Code/Game/AI/*.cpp` (pathfinding/obstacle detection)

### Outgoing
- None (header-only, no external dependencies)

## Design Patterns
- **Bitmask Flag Enum**: Uses bit flags to enable combinatorial collision type checks (e.g., `COLL_TYPE_PHYSICAL | COLL_TYPE_PROJECTILE`).
- **LSB Convention**: Forces `COLL_TYPE_ALL` (LSB) to ensure backward compatibility with legacy queries.
- **Domain-Specific Abstraction**: Encapsulates collision semantics (physical/projectile) while remaining agnostic to higher-level game logic.
