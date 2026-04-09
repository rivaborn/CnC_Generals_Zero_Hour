# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindowGlobal.cpp

## Purpose
Provides global GUI rendering functions for the game window system, acting as a bridge between the window manager and display/rendering systems.

## Responsibilities
- Wraps low-level rendering calls (images, shapes, text)
- Manages font and image lookups
- Handles color and character classification utilities
- Delegates to display and font libraries

## Key Types
- None

## Key Functions
### winDrawImage
- Purpose: Renders an image within specified screen coordinates
- Calls: TheDisplay->drawImage

### winFillRect
- Purpose: Draws a filled rectangle using absolute screen coordinates
- Calls: TheDisplay->drawFillRect

### winOpenRect
- Purpose: Draws a rectangle outline using absolute screen coordinates
- Calls: TheDisplay->drawOpenRect

### winDrawLine
- Purpose: Draws a line between two points using absolute screen coordinates
- Calls: TheDisplay->drawLine

### winFindImage
- Purpose: Looks up an image by name from the mapped image collection
- Calls: TheMappedImageCollection->findImageByName

### winMakeColor
- Purpose: Creates a color from RGBA components
- Calls: GameMakeColor

### winFindFont
- Purpose: Retrieves a font by name, size, and bold flag
- Calls: TheFontLibrary->getFont

### winIsDigit / winIsAscii / winIsAlNum
- Purpose: Character classification utilities
- Calls: GameIsDigit / GameIsAscii / GameIsAlNum

## Globals
- None

## Dependencies
- GameClient/Image.h, GameClient/Display.h, GameClient/GameWindowManager.h, GameClient/GameFont.h
- TheDisplay (Display*), TheMappedImageCollection (MappedImageCollection*), TheFontLibrary (FontLibrary*)
- GameMakeColor, GameIsDigit, GameIsAscii, GameIsAlNum
