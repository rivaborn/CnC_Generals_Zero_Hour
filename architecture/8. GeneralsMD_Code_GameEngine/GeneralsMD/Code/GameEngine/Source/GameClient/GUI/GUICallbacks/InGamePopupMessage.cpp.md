# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/InGamePopupMessage.cpp

## Purpose
Handles initialization, input, and system callbacks for an in-game popup message UI.

## Responsibilities
- Initializes popup message UI with text and layout
- Processes keyboard input (Enter/ESC) for the popup
- Manages system messages (focus, selection) for the popup window
- Handles cleanup and message clearing when dismissed

## Key Types
- None

## Key Functions
### InGamePopupMessageInit
- Purpose: Initializes the popup message UI with text, positioning, and sizing
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, TheInGameUI->getPopupMessageData, TheDisplayStringManager->newDisplayString, GadgetStaticTextSetText, TheWindowManager->winSetModal, TheWindowManager->winSetFocus, parent->winHide, parent->winBringToTop

### InGamePopupMessageInput
- Purpose: Handles keyboard input for the popup (Enter/ESC keys)
- Calls: TheWindowManager->winSendSystemMsg

### InGamePopupMessageSystem
- Purpose: Processes system messages for the popup window (create, destroy, focus, selection)
- Calls: TheMessageStream->appendMessage, TheInGameUI->clearPopupMessageData

## Globals
- parentID (NameKeyType): ID for the parent window
- staticTextMessageID (NameKeyType): ID for the static text message gadget
- buttonOkID (NameKeyType): ID for the OK button gadget
- parent (GameWindow*): Pointer to the parent window
- staticTextMessage (GameWindow*): Pointer to the static text message gadget
- buttonOk (GameWindow*): Pointer to the OK button gadget
- pause (Bool): Flag indicating if the game should pause when the popup is shown

## Dependencies
- PreRTS.h, Common/GlobalData.h, Common/NameKeyGenerator.h, Common/Version.h, Common/MessageStream.h, GameClient/WindowLayout.h, GameClient/Gadget.h, GameClient/GadgetStaticText.h, GameClient/KeyDefs.h, GameClient/GameWindowManager.h, GameClient/InGameUI.h, GameClient/DisplayStringManager.h
