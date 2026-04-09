# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLobbyMenu.cpp

## Purpose
Handles the Westwood Online (WOL) lobby menu UI and functionality in Command & Conquer Generals.

## Responsibilities
- Manages lobby UI elements (player list, game list, chat, group rooms)
- Handles player interactions (joining games, sending chat, managing buddies)
- Processes GameSpy network messages and updates
- Implements slash commands and right-click context menus
- Manages game/player list refreshing and sorting

## Key Types
- COLUMN_PLAYERNAME (Enum): Column index for player names in listbox
- rankNames (Array): String array of rank names
- TheLobbyQueuedUTMs (list<PeerResponse>): Queue of pending lobby messages

## Key Functions
### refreshGameList
- Purpose: Refreshes the list of available games
- Calls: Not inferable

### refreshPlayerList
- Purpose: Refreshes the list of players in the lobby
- Calls: Not inferable

### handleLobbySlashCommands
- Purpose: Processes slash commands entered in chat
- Calls: TheGameSpyInfo->addText, TheGameSpyInfo->sendChat

### playerTooltip
- Purpose: Generates tooltip information for players in the list
- Calls: TheMouse->setCursorTooltip, TheGameText->fetch

### populateGroupRoomListbox
- Purpose: Populates the group room dropdown with available rooms
- Calls: GadgetComboBoxReset, GadgetComboBoxAddEntry

### WOLLobbyMenuSystem
- Purpose: Main message handler for lobby menu events
- Calls: TheGameSpyPeerMessageQueue->addRequest, GSMessageBoxOk, TheGameSpyInfo->sendChat

## Globals
- isShuttingDown (Bool): Tracks if lobby is shutting down
- buttonPushed (Bool): Prevents multiple button presses
- nextScreen (char*): Next screen to transition to
- gameListRefreshTime/Interval (time_t): Game list refresh timing
- playerListRefreshTime/Interval (time_t): Player list refresh timing
- parentWOLLobbyID/buttonBackID/etc. (NameKeyType): Window IDs for UI elements
- parentWOLLobby/buttonBack/etc. (GameWindow*): Pointers to UI elements
- groupRoomToJoin (Int): Target group room for joining
- TheLobbyQueuedUTMs (list<PeerResponse>): Queue of pending lobby messages
- isThreadHosting (Bool): Tracks hosting state
- s_tryingToHostOrJoin (Bool): Prevents concurrent host/join actions

## Dependencies
- GameSpy overlay system (GameSpyOverlay.h)
- UI components (GadgetListBox, GadgetComboBox, etc.)
- Networking (PeerThread, PeerDefs)
- Game text/localization (GameText)
- Message boxes (MessageBox)
- Window management (WindowLayout, WindowManager)
