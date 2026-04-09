# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/Common/System/W3DRadar.cpp - Enhanced Analysis

## Architectural Role
This file implements the W3D-specific radar rendering system, bridging the game logic (unit positions, shroud) with the rendering pipeline (textures, coordinates). It handles the visual representation of the radar, including terrain, units, and UI elements, while coordinating with the tactical view and player systems.

## Cross-References
### Incoming
- **GameClient**: `TheDisplay->drawImage()`, `TheTacticalView` methods (view box calculations)
- **GameLogic**: `TheGameLogic->getFrame()` (for stealth unit alpha cycling)
- **PlayerSystem**: `ThePlayerList->getLocalPlayer()` (for visibility checks)

### Outgoing
- **W3DDevice**: `WW3D2/DX8Caps.h` (texture format support checks)
- **GameClient**: `SurfaceClass` methods (pixel drawing), `TextureClass` (radar textures)
- **GameLogic**: `Object` methods (unit positions, shroud status)

## Design Patterns
- **Resource Management**: Explicit texture format negotiation (`findFormat`) and cleanup (`deleteResources`), reflecting DirectX 8's resource constraints.
- **Coordinate Transformation**: `radarToPixel` and `reconstructViewBox` implement a **Projection Pattern**, converting between world, radar, and screen spaces.
- **Observer**: The radar listens to game state changes (e.g., unit movement) via implicit callbacks (not shown in code), updating its display reactively.

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns in the provided snippet.
