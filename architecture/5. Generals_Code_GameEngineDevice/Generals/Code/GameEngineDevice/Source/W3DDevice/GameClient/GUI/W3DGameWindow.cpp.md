# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/W3DGameWindow.cpp

## Purpose
Implements W3D (Westwood 3D) game window rendering, including borders, text, and default drawing behavior.

## Responsibilities
- Manages border rendering for game windows
- Handles text rendering and positioning
- Provides default draw functionality for game windows
- Initializes border image assets
- Supports various window styles (buttons, sliders, etc.)

## Key Types
- (anonymous enum): Defines border piece types (corners, lines)
- BORDER_CORNER_SIZE (Enum): Size constant for corner borders
- BORDER_LINE_SIZE (Enum): Size constant for line borders

## Key Functions
### initBorders
- Purpose: Loads border image assets from the image collection
- Calls: TheMappedImageCollection->findImageByName

### W3DGameWinDefaultDraw
- Purpose: Default redraw callback for game windows
- Calls: TheWindowManager->winDrawImage, TheWindowManager->winOpenRect, TheWindowManager->winFillRect, TheDisplay->drawVideoBuffer

### blitBorderRect
- Purpose: Draws a bordered rectangle with corners and lines
- Calls: TheDisplay->drawImage

## Globals
- bordersInit (Bool): Tracks if borders have been initialized
- borderPieces (Image*): Array holding border image references

## Dependencies
- GameClient/Gadget.h
- GameClient/GameWindowGlobal.h
- W3DDevice/GameClient/W3DGameWindow.h
- W3DDevice/GameClient/W3DGameWindowManager.h
- W3DDevice/GameClient/W3DDisplay.h
- TheMappedImageCollection (external)
- TheDisplay (external)
- TheWindowManager (external)
