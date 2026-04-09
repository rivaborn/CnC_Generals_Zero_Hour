# GeneralsMD/Code/GameEngine/Include/GameNetwork/Connection.h

## Purpose
Manages network communication queues for individual players in a multiplayer game session.

## Responsibilities
- Handles sending and receiving network commands
- Manages command queues per player
- Tracks latency and retry metrics
- Processes acknowledgments for sent commands
- Supports frame-based command grouping

## Key Types
- **Connection (Class)**: Core class managing player network connections
- **ConnectionMagicEnum (Enum)**: Not inferable (empty)
- **Connection_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### `update()`
- Purpose: Updates connection state
- Calls: Not inferable

### `doSend()`
- Purpose: Handles outgoing network commands
- Calls: Not inferable

### `doRecv()`
- Purpose: Processes incoming network commands
- Calls: Not inferable

### `sendNetCommandMsg()`
- Purpose: Sends a network command message
- Calls: Not inferable

### `processAck()`
- Purpose: Processes acknowledgment messages (multiple overloads)
- Calls: Not inferable

### `doRetryMetrics()`
- Purpose: Tracks retry metrics for reliability
- Calls: Not inferable

## Globals
- **None**

## Dependencies
- `GameNetwork/NetCommandList.h`
- `GameNetwork/User.h`
- `GameNetwork/transport.h`
- `GameNetwork/NetPacket.h`
- `MemoryPoolObject` (inheritance)
- `NetCommandMsg`, `NetAckBothCommandMsg`, `NetAckStage1CommandMsg` (external types)
