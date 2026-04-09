# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupJoinGame.cpp

## Purpose
Handles the "Join Game" popup UI, including password input and game joining logic.

## Responsibilities
- Initializes the join game popup UI
- Processes user input (keyboard and UI events)
- Handles game joining with password validation
- Manages popup lifecycle (show/hide)

## Key Types
- `None`

## Key Functions
### `PopupJoinGameInit`
- Purpose: Initializes the join game popup UI and sets up controls
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `GadgetTextEntrySetText`, `GadgetStaticTextSetText`, `TheWindowManager->winSetFocus`, `TheWindowManager->winSetModal`

### `PopupJoinGameInput`
- Purpose: Handles keyboard input for the popup (ESC key to cancel)
- Calls: `GameSpyCloseOverlay`, `SetLobbyAttemptHostJoin`

### `PopupJoinGameSystem`
- Purpose: Handles system messages for the popup (creation, destruction, button clicks, text entry)
- Calls: `GameSpyCloseOverlay`, `SetLobbyAttemptHostJoin`, `GadgetTextEntryGetText`, `GadgetTextEntrySetText`, `joinGame`

### `joinGame`
- Purpose: Attempts to join a game with the provided password
- Calls: `TheGameSpyInfo->findStagingRoomByID`, `TheGameSpyInfo->getCurrentStagingRoomID`, `TheGameSpyPeerMessageQueue->addRequest`, `GameSpyCloseOverlay`

## Globals
- `parentPopupID` (NameKeyType): ID for the parent popup window
- `textEntryGamePasswordID` (NameKeyType): ID for the password text entry field
- `buttonCancelID` (NameKeyType): ID for the cancel button
- `parentPopup` (GameWindow*): Pointer to the parent popup window
- `textEntryGamePassword` (GameWindow*): Pointer to the password text entry gadget

## Dependencies
- `PreRTS.h`, `Common/GlobalData.h`, `Common/NameKeyGenerator.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/KeyDefs.h`, `GameClient/GadgetTextEntry.h`, `GameClient/GadgetStaticText.h`, `GameNetwork/GameSpy/Peerdefs.h`, `GameNetwork/GameSpy/PeerThread.h`, `GameNetwork/GameSpyOverlay.h`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheGameSpyInfo`, `TheGameSpyPeerMessageQueue`, `GameSpyCloseOverlay`, `SetLobbyAttemptHostJoin`
