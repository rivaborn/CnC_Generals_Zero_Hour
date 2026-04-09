# GeneralsMD/Code/GameEngine/Include/GameClient/RadiusDecal.h - Enhanced Analysis

## Architectural Role
This file defines the core classes for managing circular decals (shadows) on the game map, bridging the rendering system (via `Shadow`) with game logic and network synchronization. It supports both client-side rendering and server-side state tracking for multiplayer consistency.

## Cross-References
### Incoming
- **Game Logic**: Likely called by explosion/weapon effects systems to create decals at impact points
- **Network Sync**: Used by `Xfer` system to serialize decal state for multiplayer
- **Modding**: Called by INI parsing infrastructure during map/rule loading

### Outgoing
- **Rendering**: Depends on `Shadow` class for actual decal rendering
- **Serialization**: Uses `Xfer` for network sync
- **Configuration**: Relies on `INI` parsing for template definitions

## Design Patterns
- **Template-Method**: `RadiusDecalTemplate` provides configuration while `RadiusDecal` handles runtime behavior
- **Flyweight**: Templates are reused to create multiple decal instances
- **Proxy**: `RadiusDecal` acts as a lightweight proxy to the heavier `Shadow` object

*Not inferable*: Exact relationship with `ShadowType` enum or `Player` visibility rules.
