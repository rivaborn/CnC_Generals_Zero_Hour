# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/GUICallbacks/W3DControlBar.cpp

## Purpose
Handles rendering callbacks for various UI elements in the game's control bar and HUD.

## Responsibilities
- Renders HUD elements (left/right panels, power meters)
- Draws command bar components (background, foreground, help popups)
- Displays map previews with borders
- Manages video buffer rendering for cameos and HUD

## Key Types
- None (procedural file with functions only)

## Key Functions
### W3DCameoMovieDraw
- Purpose: Renders video buffer for cameo movies
- Calls: TheInGameUI->cameoVideoBuffer(), TheDisplay->drawVideoBuffer()

### W3DLeftHUDDraw
- Purpose: Draws left HUD panel (radar or video buffer)
- Calls: ThePlayerList->getLocalPlayer(), TheRadar->draw(), TheDisplay->drawVideoBuffer()

### W3DPowerDraw
- Purpose: Renders power meter with color-coded bars
- Calls: TheMappedImageCollection->findImageByName(), TheWindowManager->winDrawImage(), TheDisplay->setClipRegion()

### W3DDrawMapPreview
- Purpose: Draws map preview with supply/tech icons and borders
- Calls: findDrawPositions(), TheDisplay->drawFillRect(), TheDisplay->drawImage(), drawSkinnyBorder()

### W3DCommandBarHelpPopupDraw
- Purpose: Renders help popup with tiled background
- Calls: TheMappedImageCollection->findImageByName(), TheWindowManager->winDrawImage()

## Globals
- None

## Dependencies
- Common/GlobalData.h, Common/Radar.h, Common/Player.h, GameClient/GameWindow.h, W3DDevice/GameClient/W3DGameWindow.h, GameClient/InGameUI.h, GameClient/Display.h, GameClient/ControlBar.h, GameClient/GameWindowManager.h, GameClient/ControlBarScheme.h, GameClient/MapUtil.h, GameLogic/GameLogic.h
