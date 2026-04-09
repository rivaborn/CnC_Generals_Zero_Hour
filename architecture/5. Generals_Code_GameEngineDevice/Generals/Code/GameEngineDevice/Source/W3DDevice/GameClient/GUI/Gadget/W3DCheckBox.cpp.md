# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DCheckBox.cpp

## Purpose
Implements rendering logic for checkbox UI controls in the SAGE engine.

## Responsibilities
- Renders checkboxes with text and optional images
- Handles different visual states (enabled/disabled/highlighted)
- Draws checkbox borders and fill colors
- Positions and draws checkbox text
- Supports both colored and image-based checkbox rendering

## Key Types
- None

## Key Functions
### drawCheckBoxText
- Purpose: Draws the text label for a checkbox
- Calls: `text->getSize()`, `text->draw()`

### W3DGadgetCheckBoxDraw
- Purpose: Renders a colored checkbox with appropriate state-based colors
- Calls: `window->winGetScreenPosition()`, `window->winGetSize()`, `GadgetCheckBoxGetDisabledColor()`, `TheWindowManager->winOpenRect()`, `TheWindowManager->winFillRect()`, `TheWindowManager->winDrawLine()`, `drawCheckBoxText()`

### W3DGadgetCheckBoxImageDraw
- Purpose: Renders a checkbox using user-supplied images for different states
- Calls: `window->winGetScreenPosition()`, `window->winGetSize()`, `GadgetCheckBoxGetDisabledCheckedBoxImage()`, `TheWindowManager->winDrawImage()`, `drawCheckBoxText()`

## Globals
- None

## Dependencies
- `GameClient/GadgetCheckBox.h`
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- `TheWindowManager` (external symbol)
- `GadgetCheckBoxGetDisabledColor()` and similar color/image getter functions
