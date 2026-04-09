# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DProjectedShadow.h - Enhanced Analysis

## Architectural Role
This file defines the core shadow rendering system for the W3D engine, bridging between the game's lighting system and the rendering pipeline. It manages dynamic shadow projection through textures, working closely with the terrain system and render objects.

## Cross-References
### Incoming
- Rendering system calls `renderShadows()` during frame rendering
- Game object system calls `addShadow()` when objects are created
- Lighting system calls `invalidateCachedLightPositions()` when lights move

### Outgoing
- Uses `TexProjectClass` for projection matrix calculations
- Interacts with `W3DShadowTextureManager` for texture management
- Depends on `RenderObjClass` for shadow casters

## Design Patterns
- **Singleton Pattern**: Global `TheW3DProjectedShadowManager` provides centralized shadow management
- **Object Pool Pattern**: Likely manages shadow textures in a pool (implied by `STT_SHARED` comment)
- **Observer Pattern**: Shadows update when lights/objects move (position tracking in `update()`)

*Not inferable*: Exact texture management strategy or decal rendering pipeline details.
