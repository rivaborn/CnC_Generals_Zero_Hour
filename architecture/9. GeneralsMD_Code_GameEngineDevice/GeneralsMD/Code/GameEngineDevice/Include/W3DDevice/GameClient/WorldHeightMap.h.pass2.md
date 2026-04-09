# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/WorldHeightMap.h - Enhanced Analysis

## Architectural Role
This file defines the core `WorldHeightMap` class, which bridges the game's terrain representation with the W3D rendering pipeline. It manages height data, texture mapping, and seismic effects, serving as the central authority for terrain queries during rendering and physics.

## Cross-References
### Incoming
- Rendering systems (e.g., `HeightMapRenderObjClass`) query UV data and height values
- Physics systems access seismic velocity and update flags
- AI pathfinding uses cliff state and height data for navigation

### Outgoing
- Calls into `TileData.h` for texture management
- Uses `WWMath/Vector3.h` for coordinate transformations
- Interfaces with `TextureClass` for terrain texture generation

## Design Patterns
- **Facade Pattern**: Exposes simplified terrain queries while hiding complex texture blending logic
- **Observer Pattern**: Seismic update flags prevent overlapping physics effects (implicit event handling)
- **Resource Pooling**: Pre-allocates tile arrays (`NUM_SOURCE_TILES`, `NUM_BLEND_TILES`) for performance

*Not inferable*: Exact memory management strategy for `m_data` and tile arrays.
