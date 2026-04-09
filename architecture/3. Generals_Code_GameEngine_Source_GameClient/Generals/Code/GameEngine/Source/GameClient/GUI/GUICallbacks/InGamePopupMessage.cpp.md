# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/InGamePopupMessage.cpp

## Purpose
Handles initialization, input, and system callbacks for an in-game popup message window.

## Responsibilities
- Initializes popup message UI elements (text, buttons)
- Processes keyboard input (ESC/ENTER) for the popup
- Manages window system messages (focus, selection)
- Controls game pause state via popup

## Key Types
- None

## Key Functions
### InGamePopupMessageInit
- Purpose: Initializes the popup message window with text and positioning
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, TheInGameUI->getPopupMessageData, TheDisplayStringManager->newDisplayString, GadgetStaticTextSetText, TheWindowManager->winSetModal, TheWindowManager->winSetFocus

### InGamePopupMessageInput
- Purpose: Handles keyboard input for the popup (ESC/ENTER keys)
- Calls: TheWindowManager->winSendSystemMsg

### InGamePopupMessageSystem
- Purpose: Processes system messages for the popup window
- Calls: TheMessageStream->appendMessage, TheInGameUI->clearPopupMessageData

## Globals
- parentID (NameKeyType): ID for the parent window
- staticTextMessageID (NameKeyType): ID for the message text window
- buttonOkID (NameKeyType): ID for the OK button
- parent (GameWindow*): Pointer to the parent window
- staticTextMessage (GameWindow*): Pointer to the message text window
- buttonOk (GameWindow*): Pointer to the OK button
- pause (Bool): Flag indicating if game should be paused

## Dependencies
- PreRTS.h, Common/GlobalData.h, Common/NameKeyGenerator.h, Common/Version.h, Common/MessageStream.h, GameClient/WindowLayout.h, GameClient/Gadget.h, GameClient/GadgetStaticText.h, GameClient/KeyDefs.h, GameClient/GameWindowManager.h, GameClient/InGameUI.h, GameClient/DisplayStringManager.h
