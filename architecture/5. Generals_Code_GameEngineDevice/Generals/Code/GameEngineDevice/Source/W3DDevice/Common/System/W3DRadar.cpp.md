# Generals/Code/GameEngineDevice/Source/W3DDevice/Common/System/W3DRadar.cpp

## Purpose
Implements the 3D radar display system for the game, handling terrain visualization, object overlays, shroud/fog-of-war, and view box rendering.

## Responsibilities
- Manages radar texture generation (terrain, overlay, shroud)
- Converts between world/radar/pixel coordinates
- Renders radar elements (icons, events, view box)
- Handles shroud updates and texture format selection

## Key Types
- `OVERLAY_REFRESH_RATE` (Enum): Frame rate for overlay updates (6 frames)
- `W3DRadar` (Class): Main radar implementation class (not shown in symbols but is the file's focus)

## Key Functions
### `legalRadarPoint`
- Purpose: Validates if a point is within radar cell bounds
- Calls: None

### `findFormat`
- Purpose: Finds a supported texture format from a list
- Calls: `DX8Caps::Support_Texture_Format`

### `initializeTextureFormats`
- Purpose: Determines optimal texture formats for radar components
- Calls: `findFormat`

### `draw`
- Purpose: Renders the complete radar display
- Calls: `findDrawPositions`, `buildTerrainTexture`, `renderObjectList`, `drawIcons`, `drawEvents`, `reconstructViewBox`, `drawViewBox`

### `setShroudLevel`
- Purpose: Updates shroud/fog-of-war for a cell
- Calls: `TheTerrainRenderObject->getShroud()`, `worldToRadar`

## Globals
- `OVERLAY_REFRESH_RATE` (const): Refresh rate constant (6)

## Dependencies
- Key includes: `W3DRadar.h`, `WW3D2/Texture.h`, `WW3D2/DX8Caps.h`, `GameLogic/TerrainLogic.h`
- External symbols: `TheTacticalView`, `TheGameLogic`, `TheDisplay`, `TheGlobalData`, `ThePlayerList`, `TheRadar`, `TheTerrainVisual`, `TheTerrainRoads`, `TheTerrainRenderObject`, `TheGameClient`, `TheMappedImageCollection`
