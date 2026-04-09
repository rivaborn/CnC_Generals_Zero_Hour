# GeneralsMD/Code/GameEngine/Source/GameNetwork/LANAPIhandlers.cpp

## Purpose
Handles LAN message callbacks for game networking, including lobby management, game joining/leaving, and in-game communication.

## Responsibilities
- Processes LAN messages (requests, announcements, chat, etc.)
- Manages player/game state in lobby and during games
- Handles game join/leave logic and validation
- Relays network events to the game via callbacks
- Manages game options and slot updates

## Key Types
- `LANAPI` (Class): Main LAN API handler class
- `LANMessage` (Struct): Message structure for LAN communication
- `LANPlayer` (Class): Represents a LAN player
- `LANGameInfo` (Class): Represents a LAN game
- `LANGameSlot` (Class): Represents a slot in a LAN game

## Key Functions
### `handleRequestLocations`
- Purpose: Handles location requests and updates player/game lists
- Calls: `fillInLANMessage`, `sendMessage`, `addPlayer`, `OnNameChange`

### `handleGameAnnounce`
- Purpose: Processes game announcements and updates game lists
- Calls: `LookupGame`, `ParseGameOptionsString`, `addGame`, `OnGameList`

### `handleRequestJoin`
- Purpose: Handles player join requests and validates game state
- Calls: `fillInLANMessage`, `sendMessage`, `OnPlayerJoin`, `RequestGameOptions`

### `handleJoinAccept`
- Purpose: Processes accepted join requests and updates game state
- Calls: `LookupGame`, `OnGameJoin`, `ParseAsciiStringToGameInfo`

### `handleChat`
- Purpose: Relays chat messages between players
- Calls: `LookupPlayer`, `OnChat`

### `handleInActive`
- Purpose: Handles player inactivity and unaccepts slots
- Calls: `GenerateGameOptionsString`, `RequestGameOptions`, `lanUpdateSlotList`

## Globals
- `TheGlobalData` (GlobalData*): Access to global game data
- `TheMapCache` (MapCache*): Access to map cache
- `TheGameState` (GameState*): Access to game state
- `TheLAN` (LANAPI*): Access to LAN API

## Dependencies
- `PreRTS.h`, `Common/CRC.h`, `Common/GameState.h`, `Common/Registry.h`, `Common/GlobalData.h`, `Common/QuotedPrintable.h`, `Common/UserPreferences.h`, `GameNetwork/LANAPI.h`, `GameNetwork/LANAPICallbacks.h`, `GameClient/MapUtil.h`
