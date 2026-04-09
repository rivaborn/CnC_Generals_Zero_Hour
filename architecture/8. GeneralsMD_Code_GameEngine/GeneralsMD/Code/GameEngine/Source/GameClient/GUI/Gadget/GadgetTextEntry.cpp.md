# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetTextEntry.cpp

## Purpose
Handles text entry GUI gadget functionality, including input processing, system messages, and font management.

## Responsibilities
- Processes keyboard and mouse input for text entry fields
- Manages system messages for text entry controls
- Handles IME (Input Method Editor) integration for non-ASCII input
- Sets and retrieves text content
- Manages font settings for text display

## Key Types
- **EntryData (struct)**: Contains text entry field data (text, position, constraints)
- **GameWindow (class)**: Base window class for GUI elements
- **UnicodeString (class)**: String type for Unicode text
- **DisplayString (class)**: Text display string with font support

## Key Functions
### GadgetTextEntryInput
- Purpose: Handles input for text entry field
- Calls: TheIMEManager->isAttachedTo, TheIMEManager->isComposing, TheWindowManager->winIsDigit, TheWindowManager->winIsAlNum, TheWindowManager->winIsAscii, TheWindowManager->winSendSystemMsg, TheWindowManager->winNextTab, TheWindowManager->winPrevTab

### GadgetTextEntrySystem
- Purpose: Handles system messages for entry field
- Calls: TheDisplayStringManager->freeDisplayString, TheWindowManager->winDestroy, TheWindowManager->winSendSystemMsg, TheIMEManager->isAttachedTo, TheIMEManager->attach

### GadgetTextEntrySetFont
- Purpose: Sets font for text entry control and its display strings
- Calls: None directly (accesses member functions)

### GadgetTextEntryGetText
- Purpose: Retrieves text from a text entry control
- Calls: TheWindowManager->winSendSystemMsg

## Globals
- **drawCnt (Byte)**: Debug counter (not used in visible code)
- **curWindow (GameWindow*)**: Tracks current input window for IME

## Dependencies
- Common/Language.h
- GameClient/DisplayStringManager.h
- GameClient/GameWindow.h
- GameClient/Gadget.h
- GameClient/GameWindowManager.h
- GameClient/IMEManager.h
- PreRTS.h
