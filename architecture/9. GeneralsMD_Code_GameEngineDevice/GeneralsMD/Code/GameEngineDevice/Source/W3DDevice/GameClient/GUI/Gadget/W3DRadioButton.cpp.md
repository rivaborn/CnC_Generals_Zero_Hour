# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DRadioButton.cpp

## Purpose
Implements rendering logic for radio button UI controls in the SAGE engine.

## Responsibilities
- Draws radio button text with appropriate colors based on state
- Renders standard colored radio button graphics
- Handles image-based radio button rendering with left/center/right image segments
- Manages visual states (enabled/disabled/highlighted/selected)

## Key Types
- None

## Key Functions
### drawRadioButtonText
- Purpose: Draws the text for a radio button with proper positioning and colors
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `text->getSize`, `text->draw`

### W3DGadgetRadioButtonDraw
- Purpose: Draws a colored radio button using standard graphics
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `TheWindowManager->winDrawLine`, `drawRadioButtonText`

### W3DGadgetRadioButtonImageDraw
- Purpose: Draws an image-based radio button using left/center/right image segments
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `TheDisplay->setClipRegion`, `TheWindowManager->winDrawImage`, `drawRadioButtonText`

## Globals
- None

## Dependencies
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `GameClient/GadgetRadioButton.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- `TheWindowManager` (external)
- `TheDisplay` (external)
