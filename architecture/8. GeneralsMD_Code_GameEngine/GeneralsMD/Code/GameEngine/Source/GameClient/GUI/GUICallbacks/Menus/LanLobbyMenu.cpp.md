# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanLobbyMenu.cpp

## Purpose
Handles the LAN lobby menu UI, including player chat, game joining/hosting, and network communication.

## Responsibilities
- Manages LAN lobby UI elements (buttons, text entries, list boxes)
- Handles player name and chat input
- Interfaces with LAN API for game creation/joining
- Manages network preferences and player settings
- Handles UI transitions and animations

## Key Types
- `LANPreferences` (Class): Stores and manages LAN-related user preferences
- `LANPlayer` (Class): Represents a player in the LAN lobby (external)
- `LANGameInfo` (Class): Contains information about a LAN game (external)

## Key Functions
### `LanLobbyMenuInit`
- Purpose: Initializes the LAN lobby menu UI and LAN API
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `TheLAN->reset`, `TheTransitionHandler->setGroup`

### `LanLobbyMenuShutdown`
- Purpose: Cleans up LAN lobby resources and saves preferences
- Calls: `prefs.write`, `DestroyGameInfoWindow`, `TheLAN->RequestLobbyLeave`, `TheShell->reverseAnimatewindow`

### `LanLobbyMenuUpdate`
- Purpose: Updates LAN lobby state and handles network updates
- Calls: `SignalUIInteraction`, `TheTransitionHandler->setGroup`, `TheLAN->update`, `MessageBoxOk`

### `LanLobbyMenuInput`
- Purpose: Handles keyboard input for the LAN lobby
- Calls: `TheWindowManager->winSendSystemMsg`

### `LanLobbyMenuSystem`
- Purpose: Handles UI system messages and button clicks
- Calls: `SignalUIInteraction`, `TheLAN->RequestGameJoin`, `TheLAN->RequestGameCreate`, `TheLAN->RequestChat`, `TheLAN->RequestSetName`

## Globals
- `LANisShuttingDown` (Bool): Tracks if LAN lobby is shutting down
- `LANbuttonPushed` (Bool): Tracks if a button was pressed
- `LANSocketErrorDetected` (Bool): Flags socket errors
- `LANnextScreen` (char*): Stores next screen to display
- `parentLanLobbyID` (NameKeyType): ID for parent window
- `buttonBackID` (NameKeyType): ID for back button
- `listboxPlayersID` (NameKeyType): ID for players list box
- `textEntryPlayerNameID` (NameKeyType): ID for player name entry
- `textEntryChatID` (NameKeyType): ID for chat entry
- `listboxChatWindowID` (NameKeyType): ID for chat window
- `listboxGamesID` (NameKeyType): ID for games list box

## Dependencies
- `LANAPI.h`, `LANGameInfo.h`, `GadgetListBox.h`, `GadgetTextEntry.h`, `MessageBox.h`, `GameWindowTransitions.h`, `ShellHooks.h`
