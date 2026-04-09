# GeneralsMD/Code/GameEngine/Include/GameNetwork/ConnectionManager.h

## Purpose
Manages network connections and message routing between players in a multiplayer game.

## Responsibilities
- Maintains connections to all players
- Queues and routes network messages
- Handles file transfers and progress tracking
- Manages packet routing and fallback plans
- Tracks bandwidth metrics and performance

## Key Types
- **ConnectionManager (Class)**: Main class for managing network connections and message routing.
- **GameInfo (Class)**: Not inferable.
- **NetCommandWrapperList (Class)**: Not inferable.
- **FileCommandMap (Class)**: Maps file command IDs to file paths.
- **FileMaskMap (Class)**: Maps file command IDs to player masks.
- **FileProgressMap (Class)**: Tracks file transfer progress per player.

## Key Functions
### `init()`
- Purpose: Initialize the connection manager.
- Calls: Not inferable.

### `update(Bool isInGame)`
- Purpose: Service all managed connections.
- Calls: Not inferable.

### `sendChat(UnicodeString text, Int playerMask, UnsignedInt executionFrame)`
- Purpose: Send a chat message to specified players.
- Calls: Not inferable.

### `sendFile(AsciiString path, UnsignedByte playerMask, UnsignedShort commandID)`
- Purpose: Initiate a file transfer to specified players.
- Calls: Not inferable.

### `processNetCommand(NetCommandRef *ref)`
- Purpose: Process an incoming network command.
- Calls: Not inferable.

### `determineRouterFallbackPlan()`
- Purpose: Establish a fallback plan for packet routing.
- Calls: Not inferable.

## Globals
- **s_fileCommandMap (FileCommandMap)**: Maps file command IDs to file paths.
- **s_fileRecipientMaskMap (FileMaskMap)**: Maps file command IDs to player masks.
- **s_fileProgressMap[MAX_SLOTS] (FileProgressMap)**: Tracks file transfer progress per player.

## Dependencies
- `GameNetwork/Connection.h`
- `GameNetwork/NetCommandList.h`
- `GameNetwork/Transport.h`
- `GameNetwork/FrameDataManager.h`
- `GameNetwork/FrameMetrics.h`
- `GameNetwork/NetworkDefs.h`
- `GameNetwork/DisconnectManager.h`
