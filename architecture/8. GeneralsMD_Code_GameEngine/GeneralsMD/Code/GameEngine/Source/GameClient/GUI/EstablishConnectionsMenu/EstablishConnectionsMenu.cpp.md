# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/EstablishConnectionsMenu/EstablishConnectionsMenu.cpp

## Purpose
Manages the UI for establishing network connections in multiplayer games.

## Responsibilities
- Displays player connection status
- Updates player names and ready buttons
- Shows/hides the connection window
- Handles connection state changes

## Key Types
- EstablishConnectionsMenu (Class): main menu class
- NATConnectionState (Enum): connection state types

## Key Functions
### initMenu
- Purpose: Shows the connection window
- Calls: ShowEstablishConnectionsWindow

### endMenu
- Purpose: Hides the connection window
- Calls: HideEstablishConnectionsWindow

### setPlayerName
- Purpose: Updates a player's name in the UI
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetStaticTextSetText

### setPlayerStatus
- Purpose: Updates a player's connection status
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetStaticTextSetText, TheGameText->fetch

## Globals
- TheEstablishConnectionsMenu (EstablishConnectionsMenu*): singleton instance
- m_playerReadyControlNames (char**): array of ready button control names
- m_playerNameControlNames (char**): array of player name control names
- m_playerStatusControlNames (char**): array of status control names

## Dependencies
- GameClient/GUICallbacks.h
- GameClient/EstablishConnectionsMenu.h
- Common/NameKeyGenerator.h
- GameClient/GameWindow.h
- GameClient/GameWindowManager.h
- GameClient/GadgetStaticText.h
- GameClient/GameText.h
