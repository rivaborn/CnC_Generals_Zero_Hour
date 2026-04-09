# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetTextEntry.cpp

## Purpose
Handles text entry input and system messages for GUI text entry fields in Command & Conquer Generals.

## Responsibilities
- Processes keyboard and mouse input for text entry
- Manages text entry constraints (numerical, alphanumerical, ASCII-only)
- Handles system messages for text entry fields
- Manages font settings for text entry controls
- Retrieves text from text entry fields

## Key Types
- EntryData (struct): Stores text entry field data including text buffers and constraints
- GadgetTextEntryInput (function): Handles input messages for text entry
- GadgetTextEntrySystem (function): Handles system messages for text entry
- GadgetTextEntrySetFont (function): Sets font for text entry control
- GadgetTextEntryGetText (function): Retrieves text from text entry field

## Key Functions
### GadgetTextEntryInput
- Purpose: Handles input messages for text entry fields
- Calls: TheWindowManager->winSendSystemMsg, TheWindowManager->winIsDigit, TheWindowManager->winIsAlNum, TheWindowManager->winIsAscii, TheWindowManager->winNextTab, TheWindowManager->winPrevTab, TheWindowManager->winSetFocus

### GadgetTextEntrySystem
- Purpose: Handles system messages for text entry fields
- Calls: TheDisplayStringManager->freeDisplayString, TheWindowManager->winDestroy, TheWindowManager->winSendSystemMsg, TheIMEManager->attach

### GadgetTextEntrySetFont
- Purpose: Sets the font for a text entry control
- Calls: None

### GadgetTextEntryGetText
- Purpose: Retrieves the text from a text entry field
- Calls: TheWindowManager->winSendSystemMsg

## Globals
- drawCnt (Byte): Not inferable (unused in visible code)
- curWindow (GameWindow*): Tracks the current input window for IME support

## Dependencies
- Common/Language.h
- GameClient/DisplayStringManager.h
- GameClient/GameWindow.h
- GameClient/Gadget.h
- GameClient/GameWindowManager.h
- GameClient/IMEManager.h
- PreRTS.h
- TheWindowManager, TheDisplayStringManager, TheIMEManager (external symbols)
