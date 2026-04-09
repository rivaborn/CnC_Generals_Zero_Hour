# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/NetworkDirectConnect.cpp

## Purpose
Handles the LAN direct connect menu UI and functionality in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages LAN direct connect UI initialization and shutdown
- Handles player name and IP address management
- Implements game hosting/joining via direct IP connection
- Updates remote IP address list from user preferences
- Processes user input for the direct connect menu

## Key Types
- **None**

## Key Functions
### PopulateRemoteIPComboBox
- Purpose: Populates the remote IP combo box with entries from user preferences.
- Calls: `GadgetComboBoxReset`, `GadgetComboBoxAddEntry`, `GadgetComboBoxSetSelectedPos`

### UpdateRemoteIPList
- Purpose: Updates the remote IP list in user preferences based on current combo box selection.
- Calls: `GadgetComboBoxGetLength`, `GadgetComboBoxGetSelectedPos`, `GadgetComboBoxGetText`, `GadgetComboBoxSetSelectedPos`

### HostDirectConnectGame
- Purpose: Initiates hosting a direct connect game using the local IP address.
- Calls: `TheLAN->RequestGameCreate`

### JoinDirectConnectGame
- Purpose: Joins a direct connect game using the selected remote IP address.
- Calls: `TheLAN->RequestGameJoinDirectConnect`, `UpdateRemoteIPList`, `PopulateRemoteIPComboBox`

### NetworkDirectConnectInit
- Purpose: Initializes the direct connect menu UI and LAN API.
- Calls: `TheLAN->init`, `TheLAN->reset`, `PopulateRemoteIPComboBox`, `TheWindowManager->winGetWindowFromId`

### NetworkDirectConnectShutdown
- Purpose: Shuts down the direct connect menu and cleans up resources.
- Calls: `TheShell->reverseAnimatewindow`, `TheTransitionHandler->reverse`

### NetworkDirectConnectUpdate
- Purpose: Updates the menu state during shutdown animations.
- Calls: `TheShell->isAnimFinished`, `TheTransitionHandler->isFinished`

### NetworkDirectConnectInput
- Purpose: Handles keyboard input for the direct connect menu.
- Calls: `TheWindowManager->winSendSystemMsg`

### NetworkDirectConnectSystem
- Purpose: Processes system messages for the direct connect menu.
- Calls: `GadgetTextEntryGetText`, `TheShell->pop`, `HostDirectConnectGame`, `JoinDirectConnectGame`

## Globals
- `LANbuttonPushed` (Bool): Tracks if LAN button was pushed.
- `LANisShuttingDown` (Bool): Tracks if LAN is shutting down.
- `isShuttingDown` (Bool): Tracks menu shutdown state.
- `buttonPushed` (Bool): Tracks button push state.
- `buttonBackID` (NameKeyType): ID for back button.
- `buttonHostID` (NameKeyType): ID for host button.
- `buttonJoinID` (NameKeyType): ID for join button.
- `editPlayerNameID` (NameKeyType): ID for player name edit box.
- `comboboxRemoteIPID` (NameKeyType): ID for remote IP combo box.
- `staticLocalIPID` (NameKeyType): ID for local IP static text.
- `buttonBack` (GameWindow*): Pointer to back button.
- `buttonHost` (GameWindow*): Pointer to host button.
- `buttonJoin` (GameWindow*): Pointer to join button.
- `editPlayerName` (GameWindow*): Pointer to player name edit box.
- `comboboxRemoteIP` (GameWindow*): Pointer to remote IP combo box.
- `staticLocalIP`
