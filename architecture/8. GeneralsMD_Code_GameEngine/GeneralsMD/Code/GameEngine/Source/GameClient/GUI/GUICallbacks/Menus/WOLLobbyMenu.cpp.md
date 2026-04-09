# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLobbyMenu.cpp

## Purpose
Handles the Westwood Online (WOL) lobby menu UI, including player/game lists, chat, and group rooms.

## Responsibilities
- Manages lobby UI elements (buttons, listboxes, chat)
- Handles player/game list refreshes and updates
- Processes lobby commands and chat messages
- Manages group room joining/leaving
- Displays player tooltips and right-click menus

## Key Types
- COLUMN_PLAYERNAME (Enum): Column index for player names in listbox
- rankNames (Array): Rank name strings for display

## Key Functions
### refreshGameList
- Purpose: Refreshes the game list display
- Calls: Not inferable

### refreshPlayerList
- Purpose: Refreshes the player list display
- Calls: Not inferable

### handleLobbySlashCommands
- Purpose: Processes slash commands in chat
- Calls: TheGameSpyInfo->addText, TheGameSpyInfo->sendChat

### playerTooltip
- Purpose: Generates tooltip for player list entries
- Calls: TheMouse->setCursorTooltip, TheGameText->fetch

### populateGroupRoomListbox
- Purpose: Populates the group room dropdown
- Calls: GadgetComboBoxReset, GadgetComboBoxAddEntry

### WOLLobbyMenuSystem
- Purpose: Main message handler for lobby UI
- Calls: TheGameSpyPeerMessageQueue->addRequest, TheGameSpyInfo->sendChat, etc.

## Globals
- isShuttingDown (Bool): Tracks shutdown state
- buttonPushed (Bool): Tracks button press state
- nextScreen (char*): Next screen to transition to
- gameListRefreshTime/Interval (time_t): Game list refresh timing
- playerListRefreshTime/Interval (time_t): Player list refresh timing
- TheLobbyQueuedUTMs (list): Queued UTM messages
- isThreadHosting (Bool): Hosting state flag

## Dependencies
- GameClient headers (WindowLayout, GadgetListBox, etc.)
- GameNetwork headers (GameSpyOverlay, PeerThread)
- Common headers (GameEngine, GameState)
- External: TheGameSpyInfo, TheWindowManager, TheMouse, etc.
