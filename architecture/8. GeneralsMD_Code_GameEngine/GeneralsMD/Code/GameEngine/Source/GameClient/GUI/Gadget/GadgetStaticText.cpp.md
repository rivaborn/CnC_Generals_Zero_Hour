# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetStaticText.cpp

## Purpose
Handles static text UI elements in the game, managing input, system messages, and text/font operations.

## Responsibilities
- Processes input for static text controls (tab navigation)
- Handles system messages (label get/set, window creation/destruction)
- Manages text and font for static text gadgets
- Memory cleanup for text data on destruction

## Key Types
- `TextData` (struct): Contains display string for static text
- `DisplayString` (class): Manages text rendering and font
- `GameFont` (class): Font resource for text rendering

## Key Functions
### `GadgetStaticTextInput`
- Purpose: Handles keyboard input for static text controls
- Calls: `window->winNextTab()`, `window->winPrevTab()`

### `GadgetStaticTextSystem`
- Purpose: Processes system messages for static text controls
- Calls: `window->winGetUserData()`, `TheDisplayStringManager->freeDisplayString()`

### `GadgetStaticTextSetText`
- Purpose: Sets the text content of a static text control
- Calls: `TheWindowManager->winSendSystemMsg()`

### `GadgetStaticTextGetText`
- Purpose: Retrieves the text content of a static text control
- Calls: `window->winGetUserData()`

### `GadgetStaticTextSetFont`
- Purpose: Updates the font for a static text control and its tooltips
- Calls: `g->winGetInstanceData()->getTextDisplayString()`, `g->winGetInstanceData()->getTooltipDisplayString()`

## Globals
- `TheDisplayStringManager` (DisplayStringManager*): Manages display strings
- `TheWindowManager` (WindowManager*): Manages game windows

## Dependencies
- `PreRTS.h`, `Language.h`, `DisplayStringManager.h`, `GameWindow.h`, `Gadget.h`, `GameWindowManager.h`
- `UnicodeString`, `WindowMsgHandledType`, `GWM_CHAR`, `GGM_GET_LABEL`, `GGM_SET_LABEL`, `GWM_CREATE`, `GWM_DESTROY`
