# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/GUICallbacks/W3DControlBar.cpp

## Purpose
Handles rendering callbacks for various UI elements in the game's control bar and HUD.

## Responsibilities
- Renders HUD elements (left/right panels, power meters)
- Draws command bar components (background, foreground, help popups)
- Handles map previews and borders
- Manages video buffer display for cameos and HUD
- Implements power meter logic with color-coded states

## Key Types
- None (procedural file with functions only)

## Key Functions
### W3DCameoMovieDraw
- Purpose: Draws video buffer for cameo movies
- Calls: TheInGameUI->cameoVideoBuffer(), TheDisplay->drawVideoBuffer()

### W3DLeftHUDDraw
- Purpose: Renders left HUD panel (radar or video buffer)
- Calls: ThePlayerList->getLocalPlayer(), TheRadar->draw(), TheDisplay->drawVideoBuffer()

### W3DPowerDraw
- Purpose: Draws power meter with color-coded states
- Calls: TheMappedImageCollection->findImageByName(), TheWindowManager->winDrawImage(), TheDisplay->setClipRegion()

### W3DDrawMapPreview
- Purpose: Renders map preview with supply/tech icons
- Calls: findDrawPositions(), TheDisplay->drawFillRect(), TheDisplay->drawImage(), drawSkinnyBorder()

### W3DCommandBarHelpPopupDraw
- Purpose: Draws help popup with tiled background
- Calls: TheMappedImageCollection->findImageByName(), TheWindowManager->winDrawImage()

## Globals
- None

## Dependencies
- Common/GlobalData.h, Common/Radar.h, Common/Player.h, GameClient/GameWindow.h
- W3DDevice/GameClient/W3DGameWindow.h, GameClient/InGameUI.h, GameClient/Display.h
- GameClient/ControlBar.h, GameClient/GameWindowManager.h, GameClient/ControlBarScheme.h
- GameClient/MapUtil.h, GameLogic/GameLogic.h
