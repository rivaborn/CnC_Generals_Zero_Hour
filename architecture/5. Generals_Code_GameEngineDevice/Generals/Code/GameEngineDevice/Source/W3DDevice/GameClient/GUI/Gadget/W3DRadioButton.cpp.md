# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DRadioButton.cpp

## Purpose
Implements rendering logic for radio button UI controls in the W3D (Westwood 3D) device layer.

## Responsibilities
- Renders radio button text and visual states (enabled/disabled/highlighted)
- Handles both colored and image-based radio button drawing
- Manages clipping regions for image-based rendering
- Applies appropriate colors/borders based on widget state

## Key Types
- None

## Key Functions
### drawRadioButtonText
- Purpose: Draws the text label for a radio button
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `text->getSize`, `text->draw`

### W3DGadgetRadioButtonDraw
- Purpose: Renders a colored radio button with appropriate state-based colors
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `TheWindowManager->winDrawLine`, `drawRadioButtonText`

### W3DGadgetRadioButtonImageDraw
- Purpose: Renders an image-based radio button with tiled center section
- Calls: `window->winGetScreenPosition`, `window->winGetSize`, `TheDisplay->setClipRegion`, `TheWindowManager->winDrawImage`, `TheDisplay->enableClipping`, `drawRadioButtonText`

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
