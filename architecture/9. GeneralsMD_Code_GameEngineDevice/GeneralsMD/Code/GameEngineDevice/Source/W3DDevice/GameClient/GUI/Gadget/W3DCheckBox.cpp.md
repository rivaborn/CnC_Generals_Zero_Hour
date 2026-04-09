# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DCheckBox.cpp

## Purpose
Implements rendering logic for checkbox UI controls in the SAGE engine.

## Responsibilities
- Renders checkboxes with text and optional images
- Handles different visual states (enabled/disabled/highlighted)
- Manages checkbox appearance based on selection state
- Draws borders, backgrounds, and checkmarks

## Key Types
- None

## Key Functions
### drawCheckBoxText
- Purpose: Draws the text label for a checkbox
- Calls: `text->getSize()`, `text->draw()`

### W3DGadgetCheckBoxDraw
- Purpose: Renders a standard colored checkbox
- Calls: `window->winGetScreenPosition()`, `window->winGetSize()`, `GadgetCheckBoxGetDisabledColor()`, `TheWindowManager->winOpenRect()`, `TheWindowManager->winFillRect()`, `TheWindowManager->winDrawLine()`, `drawCheckBoxText()`

### W3DGadgetCheckBoxImageDraw
- Purpose: Renders a checkbox using user-supplied images
- Calls: `window->winGetScreenPosition()`, `window->winGetSize()`, `GadgetCheckBoxGetDisabledCheckedBoxImage()`, `TheWindowManager->winDrawImage()`, `drawCheckBoxText()`

## Globals
- None

## Dependencies
- `GameClient/GadgetCheckBox.h`
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- `TheWindowManager` (external)
- `GadgetCheckBoxGet*` functions (external)
