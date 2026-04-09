# GeneralsMD/Code/GameEngine/Include/GameClient/EstablishConnectionsMenu.h

## Purpose
Defines the `EstablishConnectionsMenu` class for managing player connection status in multiplayer games.

## Responsibilities
- Manages UI elements for player connections
- Updates player names and connection states
- Handles menu initialization and cleanup
- Provides game abort functionality

## Key Types
- `EstablishConnectionsMenuStateType` (Enum): Menu visibility state (on/off)
- `EstablishConnectionsMenu` (Class): Main menu class for connection management

## Key Functions
### `initMenu`
- Purpose: Initializes the connection menu UI.
- Calls: Not inferable.

### `endMenu`
- Purpose: Cleans up the connection menu.
- Calls: Not inferable.

### `abortGame`
- Purpose: Aborts the current game session.
- Calls: Not inferable.

### `setPlayerName`
- Purpose: Updates a player's displayed name in the menu.
- Calls: Not inferable.

### `setPlayerStatus`
- Purpose: Updates a player's connection status in the menu.
- Calls: Not inferable.

## Globals
- `TheEstablishConnectionsMenu` (EstablishConnectionsMenu*): Singleton instance of the connection menu.

## Dependencies
- `GameNetwork/NetworkDefs.h` (for `MAX_SLOTS`, `NATConnectionState`)
- `GameNetwork/NAT.h` (for `NATConnectionState`)
- `UnicodeString` (from external library)
