# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpyGameInfo.h

## Purpose
Header for GameSpy-specific game information and slot management in the SAGE engine.

## Responsibilities
- Defines `GameSpyGameSlot` and `GameSpyGameInfo` classes for GameSpy integration
- Declares global functions for GameSpy operations (e.g., game launch, slot display)
- Manages server connections and player slots for GameSpy games

## Key Types
- **GameSpyGameSlot (Class)**: Extends `GameSlot` to store GameSpy-specific player data (profile ID, login, locale)
- **GameSpyGameInfo (Class)**: Manages GameSpy game state, slots, and server communication
- **Transport (Class)**: Forward declaration (network transport)
- **NAT (Class)**: Forward declaration (Network Address Translation)
- **None**: No enums/structs defined

## Key Functions
### `generateGameResultsPacket`
- Purpose: Generates a GameSpy results packet for game reporting.
- Calls: Not inferable (implementation in .cpp)

### `init`
- Purpose: Initializes GameSpy game info.
- Calls: Not inferable

### `startGame`
- Purpose: Marks the game as started and records the game ID.
- Calls: Not inferable

### `gotGOACall`
- Purpose: Marks the game info as queried.
- Calls: Not inferable

## Globals
- **TheGameSpyGame (GameSpyGameInfo*)**: Global instance of `GameSpyGameInfo`

## Dependencies
- `GameSpy/Peer/Peer.h` (GameSpy SDK)
- `GameNetwork/GameInfo.h` (base `GameInfo` class)
- `GameSlot` (base class for slots)
- `SBServer` (GameSpy server type)
- `AsciiString`, `Bool`, `Int`, `Un
