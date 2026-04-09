# GeneralsMD/Code/GameEngine/Include/GameClient/Shadow.h - Enhanced Analysis

## Architectural Role
This file defines the core shadow/decals system, bridging rendering (W3D) and game logic. It provides the abstract interface for shadow types and their management, used by both static and dynamic objects in the scene.

## Cross-References
### Incoming
- Rendering subsystem (uses `Shadow` interface for object shadows)
- Game object system (calls `ProjectedShadowManager` for decals)
- Shroud system (uses `enableShadowInvisible` for visibility control)

### Outgoing
- W3D rendering pipeline (via `RenderObjClass` and `RenderCost`)
- Color/math utilities (uses `Color`, `REAL_TO_INT`)

## Design Patterns
- **Factory Method**: `ProjectedShadowManager::addDecal` abstracts shadow creation
- **Strategy**: Shadow types (`SHADOW_DECAL`, etc.) encapsulate different rendering behaviors
- **Observer**: Shadows can be updated when objects/lights move (via `allowUpdates`)

*Not inferable*: Exact inheritance hierarchy of `Shadow` subclasses.
