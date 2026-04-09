# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/Common/W3DRadar.h

## Purpose
Defines the W3D radar class, handling device-specific radar rendering and logic in the SAGE engine.

## Responsibilities
- Manages radar textures (terrain, overlay, shroud)
- Handles radar drawing and event rendering
- Tracks view box and hero icon positions
- Converts between radar and pixel coordinates
- Updates shroud and terrain data

## Key Types
- **W3DRadar (Class)**: Main radar implementation with drawing and update logic.
- **TextureClass (Class)**: Forward reference for texture handling.
- **TerrainLogic (Class)**: Forward reference for terrain data.

## Key Functions
### `draw`
- Purpose: Renders the radar to screen.
- Calls: `drawEvents`, `drawIcons`, `drawViewBox`, `drawHeroIcon`.

### `buildTerrainTexture`
- Purpose: Creates the terrain texture for the radar.
- Calls: Not inferable.

### `interpolateColorForHeight`
- Purpose: Adjusts color based on terrain height.
- Calls: Not inferable.

### `radarToPixel`
- Purpose: Converts radar coordinates to pixel coordinates.
- Calls: Not inferable.

## Globals
- **m_terrainTextureFormat (WW3DFormat)**: Format for terrain texture.
- **m_overlayTextureFormat (WW3DFormat)**: Format for overlay texture.
- **m_shroudTextureFormat (WW3DFormat)**: Format for shroud texture.
- **m_textureWidth (Int)**: Width of radar textures.
- **m_textureHeight (Int)**: Height of radar textures.
- **m_reconstructViewBox (Bool)**: Flag for view box reconstruction.
- **m_viewAngle (Real)**: Camera angle for view box.
- **m_viewZoom (Real)**: Camera zoom for view box.
