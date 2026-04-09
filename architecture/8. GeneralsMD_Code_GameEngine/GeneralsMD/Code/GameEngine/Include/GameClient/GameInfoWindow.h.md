# GeneralsMD/Code/GameEngine/Include/GameClient/GameInfoWindow.h

## Purpose
Header file declaring functions for managing the LAN game info window in the game client.

## Responsibilities
- Declares functions for creating, destroying, refreshing, and hiding the game info window
- Provides interface for displaying LAN game information to the player
- Serves as a bridge between the game client UI and LAN game data

## Key Types
None

## Key Functions
### CreateLANGameInfoWindow
- Purpose: Creates the LAN game info window with specified size and position
- Calls: Not inferable

### DestroyGameInfoWindow
- Purpose: Destroys the game info window
- Calls: Not inferable

### RefreshGameInfoWindow
- Purpose: Updates the game info window with new game data
- Calls: Not inferable

### HideGameInfoWindow
- Purpose: Shows or hides the game info window
- Calls: Not inferable

## Globals
None

## Dependencies
- GameClient/GameWindow.h
- GameNetwork/LANGameInfo.h
- Uses GameWindow, GameInfo, UnicodeString, Bool types from included headers
