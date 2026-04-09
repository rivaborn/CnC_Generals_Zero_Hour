# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupJoinGame.cpp

## Purpose
Handles the "Join Game" popup UI, including password input and game joining logic.

## Responsibilities
- Initializes the join game popup UI
- Processes user input (keyboard and button clicks)
- Handles system messages for the popup
- Validates and submits the game password
- Manages the game joining process via GameSpy

## Key Types
- `GameWindow` (Type): UI window handle
- `NameKeyType` (Type): UI element identifier
- `PeerRequest` (Struct): Network request for joining a game
- `GameSpyStagingRoom` (Class): Represents a game lobby/staging room

## Key Functions
### `PopupJoinGameInit`
- Purpose: Initializes the join game popup UI elements
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `GadgetTextEntrySetText`, `GadgetStaticTextSetText`, `TheWindowManager->winSetFocus`, `TheWindowManager->winSetModal`

### `PopupJoinGameInput`
- Purpose: Handles keyboard input for the popup
- Calls: `GameSpyCloseOverlay`, `SetLobbyAttemptHostJoin`

### `PopupJoinGameSystem`
- Purpose: Processes system messages for the popup
- Calls: `GadgetTextEntryGetText`, `GadgetTextEntrySetText`, `joinGame`, `GameSpyCloseOverlay`, `SetLobbyAttemptHostJoin`

### `joinGame`
- Purpose: Submits the join game request with the provided password
- Calls: `TheGameSpyInfo->findStagingRoomByID`, `TheGameSpyInfo->getCurrentStagingRoomID`, `TheGameSpyPeerMessageQueue->addRequest`, `GameSpyCloseOverlay`

## Globals
- `parentPopupID` (NameKeyType): ID for the parent popup window
- `textEntryGamePasswordID` (NameKeyType): ID for the password text entry field
- `buttonCancelID` (NameKeyType): ID for the cancel button
- `parentPopup` (GameWindow*): Pointer to the parent popup window
- `textEntryGamePassword` (GameWindow*): Pointer to the password text entry field

## Dependencies
- `PreRTS.h`, `Common/GlobalData.h`, `Common/NameKeyGenerator.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/KeyDefs.h`, `GameClient/GadgetTextEntry.h`, `GameClient/GadgetStaticText.h`, `GameNetwork/GameSpy/Peerdefs.h`, `GameNetwork/GameSpy/PeerThread.h`, `GameNetwork
