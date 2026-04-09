# GeneralsMD/Code/GameEngine/Include/GameClient/DrawableInfo.h - Enhanced Analysis

## Architectural Role
This header defines the bridge between the W3D rendering system and the game's object hierarchy, enabling the engine to manage render state (occlusion, transparency) while maintaining references to game objects and their "ghost" (fogged) counterparts.

## Cross-References
### Incoming
- Rendering subsystem (uses `ExtraRenderFlags` for occlusion/transparency logic)
- Game object system (references `ObjectID` for shroud status)
- Drawable management (holds `Drawable` and `GhostObject` pointers)

### Outgoing
- None (pure data structure with no external calls)

## Design Patterns
- **Data Transfer Object (DTO)**: Encapsulates render-related data for transfer between subsystems
- **Bitmask Flags**: Uses `ExtraRenderFlags` for compact render state representation
- **Forward Declaration**: Minimizes dependencies via class forward declarations

*Not inferable: No inheritance or behavioral patterns evident in this header-only structure.*
