# GeneralsMD/Code/GameEngine/Include/GameNetwork/DisconnectManager.h

## Purpose
Manages player disconnections, timeouts, and voting in multiplayer games.

## Responsibilities
- Handles disconnect detection and voting
- Manages packet router fallback logic
- Tracks player timeouts and frame synchronization
- Coordinates disconnect screen display

## Key Types
- **DisconnectStateType (Enum)**: Disconnect screen state (on/off)
- **DisconnectVoteStruct (Struct)**: Stores vote and frame data
- **DisconnectManager (Class)**: Core disconnect management class

## Key Functions
### `processDisconnectCommand`
- Purpose: Processes incoming disconnect commands
- Calls: `processDisconnectKeepAlive`, `processDisconnectPlayer`, etc.

### `voteForPlayerDisconnect`
- Purpose: Initiates a disconnect vote for a player
- Calls: `sendVoteCommand`

### `updateDisconnectStatus`
- Purpose: Updates disconnect state based on current conditions
- Calls: `hasPlayerTimedOut`, `isPlayerVotedOut`

### `sendKeepAlive`
- Purpose: Sends keep-alive packets to detect disconnections
- Calls: None visible

## Globals
- **m_playerTimeouts (time_t[MAX_SLOTS-1])**: Tracks timeout times per player
- **m_packetRouterTimeout (time_t)**: Tracks packet router timeout
- **m_disconnectFrames (UnsignedInt[MAX_SLOTS])**: Stores disconnect frame per player

## Dependencies
- `GameNetwork/NetCommandRef.h`
- `Lib/BaseType.h`
- `ConnectionManager` (forward declared)
