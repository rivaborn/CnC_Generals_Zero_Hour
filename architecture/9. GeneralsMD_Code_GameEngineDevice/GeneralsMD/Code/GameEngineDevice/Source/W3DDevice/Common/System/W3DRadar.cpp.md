# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/Common/System/W3DRadar.cpp

## Purpose
Implements the W3D radar system for the game, handling terrain visualization, object overlays, shroud rendering, and view box calculations.

## Responsibilities
- Manages radar texture formats and resources
- Renders terrain, objects, and shroud on the radar
- Handles coordinate conversions between world, radar, and screen spaces
- Draws radar-specific UI elements (view box, hero icons, events)
- Updates radar display based on game state and camera settings

## Key Types
- `OVERLAY_REFRESH_RATE` (Enum): Defines how often the overlay texture is refreshed (6 frames)
- `W3DRadar` (Class): Main radar implementation class (not shown in symbols but referenced in code)

## Key Functions
### `legalRadarPoint`
- Purpose: Checks if a radar coordinate is within valid bounds
- Calls: None

### `findFormat`
- Purpose: Finds a supported texture format from a list of candidates
- Calls: `DX8Wrapper::Get_Current_Caps()->Support_Texture_Format()`

### `initializeTextureFormats`
- Purpose: Initializes supported texture formats for terrain, overlay, and shroud
- Calls: `findFormat()`

### `deleteResources`
- Purpose: Releases radar-specific resources
- Calls: `Release_Ref()`, `deleteInstance()`

### `reconstructViewBox`
- Purpose: Recalculates the view box based on current camera settings
- Calls: `TheTacticalView->getScreenCornerWorldPointsAtZ()`, `TheTacticalView->getAngle()`, `TheTacticalView->getPosition()`, `TheTacticalView->getZoom()`

### `radarToPixel`
- Purpose: Converts radar coordinates to screen pixel coordinates
- Calls: None

### `draw`
- Purpose: Renders the complete radar display
- Calls: `ThePlayerList->getLocalPlayer()`, `findDrawPositions()`, `TheDisplay->drawImage()`, `renderObjectList()`, `drawIcons()`, `drawEvents()`, `reconstructViewBox()`, `drawViewBox()`

### `buildTerrainTexture`
- Purpose: Generates the terrain texture for the radar
- Calls: `TheTerrainRenderObject->getHeightMap()`, `TheTerrainRenderObject->getWater()`, `TheTerrainRenderObject->getTerrainVisual()`, `surface->DrawPixel()`

### `setShroudLevel`
- Purpose: Updates shroud visibility for a specific cell
- Calls: `TheTerrainRenderObject->getShroud()`, `surface->DrawPixel()`

## Globals
- `OVERLAY_REFRESH_RATE` (const Int): Refresh rate for overlay texture (6 frames)

## Dependencies
- Key includes: `Common/AudioEventRTS.h`, `Common/Debug.h`, `Common/GlobalData.h`, `Common/Player.h`, `Common/PlayerList.h`, `GameLogic/TerrainLogic.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameClient/Color.h`, `GameClient/Display.h`, `GameClient/GameClient.h`, `GameClient/GameWindow.h`, `GameClient/Image.h`, `GameClient/Line2D.h`, `GameClient/TerrainVisual.h`, `GameClient/Water.h`, `W3DDevice/Common/W3DRadar.h`, `W3DDevice/GameClient/HeightMap.h`, `W3DDevice/GameClient/W3DShroud.h`, `WW3D2/Texture.h`, `WW3D2/DX8Caps.h`
- External symbols: `TheTacticalView`, `TheMappedImage
