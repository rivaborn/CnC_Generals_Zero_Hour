# Generals/Code/GameEngineDevice/Include/W3DDevice/Common/W3DRadar.h

## Purpose
Defines the W3DRadar class, handling device-specific radar rendering in the W3D engine.

## Responsibilities
- Manages radar textures (terrain, overlay, shroud)
- Renders radar elements (icons, events, view box)
- Handles shroud updates and terrain refresh
- Converts between radar and pixel coordinates
- Caches hero positions for icon rendering

## Key Types
- **W3DRadar (Class)**: Main radar rendering class extending Radar.
- **TextureClass (Class)**: Forward reference for texture handling.
- **TerrainLogic (Class)**: Forward reference for terrain data.

## Key Functions
### `draw`
- Purpose: Renders the radar to screen.
- Calls: `drawEvents`, `drawIcons`, `drawViewBox`, etc.

### `buildTerrainTexture`
- Purpose: Creates the terrain texture for the radar.
- Calls: Not inferable (implementation in .cpp).

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
- **m_textureWidth/Height (Int)**: Dimensions for radar textures.
- **m_reconstructViewBox (Bool)**: Flag for view box updates.
- **m_viewAngle/Zoom (Real)**: Camera properties for view box.
- **m_viewBox (ICoord2D[4])**: Radar cell points for
