# Generals/Code/Tools/matchbot/matcher.cpp

## Purpose
Handles peer-to-peer matchmaking and room management for the game's matchmaking system.

## Responsibilities
- Manages peer connections and room joining
- Handles various peer callbacks (disconnect, messages, player events)
- Implements matchmaking logic via `checkMatches()`
- Manages nickname conflicts and CD key authentication
- Rotates logs based on configuration

## Key Types
- **MatcherClass (Class)**: Main class handling matchmaking logic
- **PEER (Type)**: Opaque peer connection handle
- **RoomType (Enum)**: Room type identifiers (TitleRoom, GroupRoom, StagingRoom)
- **MessageType (Enum)**: Message type identifiers

## Key Functions
### `logIt`
- Purpose: Writes log messages to "logIt.txt"
- Calls: `fopen`, `fputs`, `fclose`

### `readLoop`
- Purpose: Main loop for peer connection and matchmaking
- Calls: `peerThink`, `peerIsConnected`, `checkMatches`, `msleep`, `rotateOutput`, `rotateParanoid`

### `DisconnectedCallback`
- Purpose: Handles peer disconnection events
- Calls: `handleDisconnect`

### `NickErrorCallback`
- Purpose: Handles nickname errors and retries with modified nicknames
- Calls: `peerRetryWithNick`, `handleNickError`

### `connectAndLoop`
- Purpose: Initializes peer connection and starts matchmaking loop
- Calls: `init`, `peerInitialize`, `peerSetTitle`, `peerConnect`, `peerAuthenticateCDKey`, `peerListGroupRooms`, `peerJoinGroupRoom`, `readLoop`, `peerDisconnect`, `peerShutdown`

## Globals
- **s_groupID (int)**: Stores the group ID for the "QuickMatch" room

## Dependencies
- Key includes: `global.h`, `matcher.h`, `encrypt.h`, `timezone.h`, `debug.h`
- External symbols: `peerInitialize`, `peerSetTitle`, `peerConnect`, `peerAuthenticateCDKey`, `peerListGroupRooms`, `peerJoinGroupRoom`, `peerEnumPlayers`, `peerDisconnect`, `peerShutdown`, `peerThink`, `peerIsConnected`, `peerRetryWithNick`, `Global.config`, `DBGMSG`, `INFMSG`, `ERRMSG`
