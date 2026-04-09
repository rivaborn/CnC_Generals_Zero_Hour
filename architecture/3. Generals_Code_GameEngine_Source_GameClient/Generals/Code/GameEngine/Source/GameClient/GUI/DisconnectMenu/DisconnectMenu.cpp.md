# Generals/Code/GameEngine/Source/GameClient/GUI/DisconnectMenu/DisconnectMenu.cpp

## Purpose
Manages the in-game disconnect menu UI, handling player disconnections, voting, and chat.

## Responsibilities
- Controls visibility and state of disconnect menu UI elements
- Updates player names, timeouts, and vote counts
- Manages chat display and sending
- Handles player removal and voting logic

## Key Types
- **DisconnectMenu (Class)**: Main class managing disconnect menu functionality
- **DISCONNECTMENUSTATETYPE (Enum)**: Tracks menu state (on/off)

## Key Functions
### showScreen
- Purpose: Displays the disconnect menu and hides other UI elements
- Calls: HideDiplomacy, HideInGameChat, HideQuitMenu, ShowDisconnectWindow

### setPlayerName
- Purpose: Updates player name display for a specific slot
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetStaticTextSetText

### voteForPlayer
- Purpose: Sends a vote to disconnect a specific player
- Calls: TheNetwork->voteForPlayerDisconnect

### showChat
- Purpose: Displays chat messages in the disconnect menu
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetListBoxAddEntryText

## Globals
- **chatNormalColor (Color)**: Default color for chat text
- **TheDisconnectMenu (DisconnectMenu**)**: Singleton instance of the disconnect menu

## Dependencies
- GameClient headers: DisconnectMenu.h, GUICallbacks.h, GameWindow.h, GameWindowManager.h, GadgetStaticText.h, GadgetListBox.h, GameText.h
- GameNetwork headers: GameInfo.h, NetworkInterface.h
- Common header: NameKeyGenerator.h
