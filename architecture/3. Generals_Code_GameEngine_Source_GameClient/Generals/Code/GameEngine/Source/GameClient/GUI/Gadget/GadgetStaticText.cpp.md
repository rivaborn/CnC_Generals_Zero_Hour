# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetStaticText.cpp

## Purpose
Implements a static text gadget for the game's UI, handling input, system messages, and text/font management.

## Responsibilities
- Handles keyboard input for static text controls
- Manages system messages (creation, destruction, label get/set)
- Provides functions to set/get text and font for static text gadgets

## Key Types
- `TextData` (struct): Not inferable.
- `DisplayString` (class): Not inferable.
- `GameFont` (class): Not inferable.

## Key Functions
### GadgetStaticTextInput
- Purpose: Handles keyboard input for static text controls (tab navigation).
- Calls: `window->winNextTab()`, `window->winPrevTab()`

### GadgetStaticTextSystem
- Purpose: Processes system messages for static text controls (creation, destruction, label management).
- Calls: `TheDisplayStringManager->freeDisplayString()`, `tData->text->getText()`, `tData->text->setText()`

### GadgetStaticTextSetText
- Purpose: Sets the text content of a static text control.
- Calls: `TheWindowManager->winSendSystemMsg()`

### GadgetStaticTextGetText
- Purpose: Retrieves the text content of a static text control.
- Calls: None.

### GadgetStaticTextSetFont
- Purpose: Updates the font for a static text control and its associated display strings.
- Calls: `dString->setFont()`

## Globals
- `TheDisplayStringManager` (DisplayStringManager*): Manages display strings.
- `TheWindowManager` (WindowManager*): Manages game windows.

## Dependencies
- `PreRTS.h`, `Language.h`, `DisplayStringManager.h`, `GameWindow.h`, `Gadget.h`, `GameWindowManager.h`
- `UnicodeString`, `WindowMsgHandledType`, `GameWindow`, `TextData`, `DisplayString`, `GameFont`
