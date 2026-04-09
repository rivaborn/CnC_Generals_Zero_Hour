# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DStaticText.cpp

## Purpose
Implements rendering for static text GUI controls in the W3D (W3D) device layer.

## Responsibilities
- Renders static text with optional background/borders
- Handles text wrapping and alignment
- Supports both colored and image-based backgrounds
- Manages text clipping and hotkey highlighting

## Key Types
- `TextData` (struct): Stores text rendering parameters (not shown in file)
- `WinInstanceData` (struct): Window instance data (external)
- `GameWindow` (class): Base window class (external)

## Key Functions
### `drawStaticTextText`
- Purpose: Renders text content with wrapping and alignment
- Calls: `text->setWordWrap`, `text->setWordWrapCentered`, `text->setUseHotkey`, `text->getSize`, `text->setClipRegion`, `text->draw`

### `W3DGadgetStaticTextDraw`
- Purpose: Draws static text with colored background/border
- Calls: `GadgetStaticTextGetDisabledColor`, `GadgetStaticTextGetDisabledBorderColor`, `GadgetStaticTextGetEnabledColor`, `GadgetStaticTextGetEnabledBorderColor`, `TheWindowManager->winOpenRect`, `TheWindowManager->winFillRect`, `drawStaticTextText`

### `W3DGadgetStaticTextImageDraw`
- Purpose: Draws static text with image-based background
- Calls: `GadgetStaticTextGetDisabledImage`, `GadgetStaticTextGetEnabledImage`, `TheWindowManager->winDrawImage`, `drawStaticTextText`

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
- External symbols: `TheGlobalData`, `TheWindowManager`, `GadgetStaticTextGetDisabledColor`, `GadgetStaticTextGetDisabledBorderColor`, `GadgetStaticTextGetEnabledColor`, `GadgetStaticTextGetEnabledBorderColor`, `GadgetStaticTextGetDisabledImage`, `GadgetStaticTextGetEnabledImage`
