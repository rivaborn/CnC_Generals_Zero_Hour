# Generals/Code/Libraries/Source/WWVegas/WW3D2/coltype.h - Enhanced Analysis

## Architectural Role
This header defines the collision type bit-field system used by the W3D rendering subsystem for spatial queries. It enables selective collision detection between different object types (e.g., physical bodies vs. projectiles) by providing a low-level masking mechanism.

## Cross-References
### Incoming
- W3D rendering objects (e.g., `Model.cpp`, `Scene.cpp`) use these collision types for spatial queries
- AI pathfinding (`Pathfinder.cpp`) references collision types for navigation mesh queries
- Game logic collision detection systems consume these types

### Outgoing
- None (header-only, no external dependencies)

## Design Patterns
- **Bitmask Flag Enum**: Uses bit flags to enable combinatorial collision type queries
- **Type-Safe Masking**: Enforces collision type separation (physical vs. projectile) via LSB requirement
- **Not inferable**: No other patterns evident from header alone
