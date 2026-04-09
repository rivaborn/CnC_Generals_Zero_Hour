# Generals/Code/GameEngineDevice/Source/W3DDevice/Common/System/W3DRadar.cpp - Enhanced Analysis

## Architectural Role
This file implements the W3D-specific radar rendering system, bridging the game logic's radar data with the rendering pipeline. It handles texture management, coordinate transformations, and visual effects like shroud/fog-of-war, serving as the concrete implementation of the abstract `Radar` class for the W3D graphics backend.

## Cross-References
### Incoming
- **GameClient**: Calls `draw()` during UI rendering
- **TerrainLogic**: Triggers `refreshTerrain()` on map changes
- **Player**: Checks `hasRadar()` for visibility rules
- **TacticalView**: Provides zoom/angle for view box rendering

### Outgoing
- **WW3D2**: Uses `Texture` and `DX8Caps` for texture management
- **GameClient**: Delegates to `TheDisplay` for primitive rendering
- **GameLogic**: Queries `TheTerrainRenderObject` for shroud data
- **W3DDevice**: Calls `W3DShroud` for fog-of-war updates

## Design Patterns
- **Strategy Pattern**: Texture format selection via `findFormat()` allows runtime adaptation to hardware capabilities
- **Observer Pattern**: Listens to terrain/logic changes to update radar display
- **Decorator Pattern**: Overlay/shroud textures are composited on top of terrain base layer

*Not inferable*: Exact implementation of `renderObjectList()` or `buildTerrainTexture()` visibility.
