# GeneralsMD/Code/GameEngine/Source/Common/RTS/PlayerList.cpp

## Purpose
Manages the list of players in the game, including their creation, initialization, and relationships.

## Responsibilities
- Maintains a list of Player objects
- Handles player relationships (allies/enemies/neutral)
- Manages local player switching
- Serializes player data for save/load
- Updates player states each frame

## Key Types
- **PlayerList (Class)**: Manages all players in the game
- **Player (Class)**: Represents an individual player (external)
- **Team (Class)**: Represents player teams (external)
- **PlayerMaskType (Type)**: Bitmask for player identification

## Key Functions
### `newGame()`
- Purpose: Initializes players for a new game from side data
- Calls: `init()`, `Player::initFromDict()`, `TheTeamFactory->initFromSides()`, `findPlayerWithNameKey()`

### `setLocalPlayer(Player *player)`
- Purpose: Sets the current local player and notifies previous/local players
- Calls: `Player::becomingLocalPlayer()`

### `getPlayersWithRelationship(Int srcPlayerIndex, UnsignedInt allowedRelationships)`
- Purpose: Returns a bitmask of players matching specified relationships
- Calls: `getNthPlayer()`, `Player::getRelationship()`

### `xfer(Xfer *xfer)`
- Purpose: Serializes player data for save/load
- Calls: `Xfer::xferInt()`, `Xfer::xferSnapshot()`

## Globals
- **ThePlayerList (PlayerList*)**: Global instance of the player list

## Dependencies
- `Player.h`, `PlayerList.h`, `Team.h`, `Xfer.h`
- `TheSidesList`, `TheTeamFactory`, `TheNetwork`, `TheNameKeyGenerator` (external globals)
- `DEBUG_LOG`, `DEBUG_CRASH` (debug macros)
