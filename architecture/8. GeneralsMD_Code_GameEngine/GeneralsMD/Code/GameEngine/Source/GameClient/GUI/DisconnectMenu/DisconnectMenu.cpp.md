# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/DisconnectMenu/DisconnectMenu.cpp

## Purpose
Manages the in-game disconnect menu UI, handling player disconnections, voting, and chat.

## Responsibilities
- Controls visibility and state of disconnect menu UI elements
- Updates player names, timeouts, and vote counts
- Manages chat display and sending
- Handles player removal and voting logic

## Key Types
- **DisconnectMenu (Class)**: Main class managing the disconnect menu UI
- **DISCONNECTMENUSTATETYPE (Enum)**: Tracks menu state (on/off)

## Key Functions
### `showScreen()`
- Purpose: Displays the disconnect menu and hides other menus
- Calls: `HideDiplomacy()`, `HideInGameChat()`, `HideQuitMenu()`, `ShowDisconnectWindow()`

### `setPlayerName()`
- Purpose: Updates player name display for a specific slot
- Calls: `GadgetStaticTextSetText()`, `showPlayerControls()`, `hidePlayerControls()`

### `voteForPlayer()`
- Purpose: Sends vote for disconnecting a specific player
- Calls: `TheNetwork->voteForPlayerDisconnect()`

### `showChat()`
- Purpose: Displays chat message in the menu's list box
- Calls: `GadgetListBoxAddEntryText()`

## Globals
- **chatNormalColor (Color)**: Default color for chat text
- **TheDisconnectMenu (DisconnectMenu*)**: Singleton instance of the disconnect menu

## Dependencies
- `DisconnectMenu.h`, `GUICallbacks.h`, `NameKeyGenerator.h`, `GameWindow.h`, `GameWindowManager.h`, `GadgetStaticText.h`, `GadgetListBox.h`, `GameText.h`, `NetworkInterface.h`
- Uses `TheNameKeyGenerator`, `TheWindowManager`, `TheNetwork`, `TheGameText` globals
