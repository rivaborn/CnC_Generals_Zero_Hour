# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/StagingRoomGameInfo.h

## Purpose
Defines GameSpy-specific game information classes for managing multiplayer game sessions.

## Responsibilities
- Manages GameSpy game slots with player stats and connection details
- Handles staging room game state (password, observers, version checks)
- Generates GameSpy and ladder game result packets
- Tracks game host status and local player slot

## Key Types
- **GameSpyGameSlot (Class)**: Extends GameSlot to store GameSpy-specific player data (profile ID, login, locale, wins/losses, ping, rank points).
- **GameSpyStagingRoom (Class)**: Extends GameInfo to manage GameSpy game session details (game name, ID, transport, player slots, ladder info).

## Key Functions
### `generateGameSpyGameResultsPacket`
- Purpose: Creates a GameSpy-formatted results packet for game completion.
- Calls: Not inferable (implementation in .cpp).

### `generateLadderGameResultsPacket`
- Purpose: Creates a ladder-specific results packet.
- Calls: Not inferable.

### `amIHost`
- Purpose: Checks if the local player is the game host.
- Calls: Not inferable.

### `startGame`
- Purpose: Marks the game as started and records the game ID.
- Calls: Not inferable.

### `launchGame`
- Purpose: Initiates game launch after NAT negotiation.
- Calls: Not inferable.

## Globals
- **TheGameSpyGame (GameSpyStagingRoom*)**: Global pointer to the active GameSpy staging room instance.

## Dependencies
- `GameNetwork/GameInfo.h` (base class)
- `GameNetwork/Transport.h` (transport layer)
- `AsciiString`, `UnicodeString`, `Bool` (primitive types)
