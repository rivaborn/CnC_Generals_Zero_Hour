# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/W3DGameWindow.cpp

## Purpose
Implements W3D-specific game window rendering, including borders, text, and default draw functionality.

## Responsibilities
- Manages border rendering for game windows
- Handles text rendering and positioning
- Provides default draw callback for game windows
- Initializes border image assets

## Key Types
- (anonymous enum): Border piece constants (BORDER_CORNER_SIZE, BORDER_LINE_SIZE)
- BORDER_CORNER_SIZE (Enum): Corner size constant (15)
- BORDER_LINE_SIZE (Enum): Line size constant (20)

## Key Functions
### initBorders
- Purpose: Loads border image assets from image collection
- Calls: TheMappedImageCollection->findImageByName

### W3DGameWinDefaultDraw
- Purpose: Default redraw callback for game windows
- Calls: winGetScreenPosition, winGetSize, winDrawImage, winOpenRect, winFillRect, TheDisplay->drawVideoBuffer

### blitBorderRect
- Purpose: Draws border rectangle with corners and lines
- Calls: TheDisplay->drawImage

## Globals
- bordersInit (Bool): Tracks if borders are initialized
- borderPieces (Image*): Array of border image assets

## Dependencies
- GameClient/Gadget.h
- GameClient/GameWindowGlobal.h
- W3DDevice/GameClient/W3DGameWindow.h
- W3DDevice/GameClient/W3DGameWindowManager.h
- W3DDevice/GameClient/W3DDisplay.h
