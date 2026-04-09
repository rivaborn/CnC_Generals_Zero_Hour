# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanLobbyMenu.cpp

## Purpose
Handles the LAN lobby menu UI, including player chat, game listing, and connection management.

## Responsibilities
- Manages LAN lobby UI elements (buttons, text entries, list boxes)
- Handles player name and chat input
- Interfaces with LAN API for game creation/joining
- Manages network preferences and player settings
- Handles UI transitions and input events

## Key Types
- `LANPreferences` (Class): Manages LAN-related user preferences (name, color, faction, etc.)
- `playerTooltip` (Function): Displays tooltips for players in the list box

## Key Functions
### `LanLobbyMenuInit`
- Purpose: Initializes the LAN lobby menu and LAN API
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `TheLAN->init`, `TheLAN->SetLocalIP`

### `LanLobbyMenuShutdown`
- Purpose: Cleans up LAN lobby resources and saves preferences
- Calls: `prefs.write`, `TheLAN->RequestLobbyLeave`, `TheShell->reverseAnimatewindow`

### `LanLobbyMenuUpdate`
- Purpose: Updates LAN lobby state and handles animations
- Calls: `TheLAN->update`, `TheTransitionHandler->isFinished`, `shutdownComplete`

### `LanLobbyMenuInput`
- Purpose: Handles keyboard input for the LAN lobby
- Calls: `TheWindowManager->winSendSystemMsg`

### `LanLobbyMenuSystem`
- Purpose: Handles system messages for the LAN lobby UI
- Calls: `TheLAN->RequestGameJoin`, `TheLAN->RequestGameCreate`, `TheLAN->RequestChat`, `TheLAN->RequestSetName`

## Globals
- `LANisShuttingDown` (Bool): Tracks if LAN lobby is shutting down
- `LANbuttonPushed` (Bool): Tracks if a button was pressed
- `LANSocketErrorDetected` (Bool): Tracks socket errors
- `LANnextScreen` (char*): Stores the next screen to display
- `parentLanLobbyID` (NameKeyType): ID for the parent lobby window
- `listboxChatWindowID` (NameKeyType): ID for the chat window list box
- `useFpsLimit` (Bool): Tracks FPS limit setting
- `defaultName` (UnicodeString): Default player name

## Dependencies
- `LANAPI.h`, `GadgetListBox.h`, `GadgetTextEntry.h`, `MessageBox.h`, `WindowLayout.h`
- `TheLAN`, `TheWindowManager`, `TheGameText`, `TheMouse`, `TheShell`, `TheTransitionHandler`
