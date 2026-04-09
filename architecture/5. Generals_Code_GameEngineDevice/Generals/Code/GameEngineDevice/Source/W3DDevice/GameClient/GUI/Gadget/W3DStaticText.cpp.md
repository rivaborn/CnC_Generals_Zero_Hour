# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DStaticText.cpp

## Purpose
Implements rendering for static text GUI controls in the W3D (Westwood 3D) device layer.

## Responsibilities
- Renders static text with or without background images
- Handles text positioning, clipping, and word wrapping
- Applies different colors based on enabled/disabled state
- Draws borders and background fills for text fields

## Key Types
- `TextData` (struct): Contains text and formatting data for the gadget
- `WinInstanceData` (struct): Window instance data (external)
- `GameWindow` (class): Base window class (external)

## Key Functions
### `drawStaticTextText`
- Purpose: Renders the actual text content of a static text control
- Calls: `text->setWordWrap`, `text->setWordWrapCentered`, `text->getSize`, `text->setClipRegion`, `text->draw`

### `W3DGadgetStaticTextDraw`
- Purpose: Draws a static text field with colored background and border
- Calls: `GadgetStaticTextGetDisabledColor`, `GadgetStaticTextGetDisabledBorderColor`, `GadgetStaticTextGetEnabledColor`, `GadgetStaticTextGetEnabledBorderColor`, `drawStaticTextText`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`

### `W3DGadgetStaticTextImageDraw`
- Purpose: Draws a static text field with a background image
- Calls: `GadgetStaticTextGetDisabledImage`, `GadgetStaticTextGetEnabledImage`, `drawStaticTextText`, `TheWindowManager->winDrawImage`

## Globals
- None

## Dependencies
- `Common/GlobalData.h`
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `GameClient/GadgetStaticText.h`
- `W3DDevice/GameClient/W3DGameWindow.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
- External symbols: `GadgetStaticTextGetDisabledColor`, `GadgetStaticTextGetDisabledBorderColor`, `GadgetStaticTextGetEnabledColor`, `GadgetStaticTextGetEnabledBorderColor`, `GadgetStaticTextGetDisabledImage`, `GadgetStaticTextGetEnabledImage`, `TheWindowManager`, `TheGlobalData`
