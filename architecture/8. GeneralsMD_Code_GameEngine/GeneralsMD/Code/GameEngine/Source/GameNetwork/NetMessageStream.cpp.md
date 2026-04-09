# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetMessageStream.cpp

## Purpose
Handles encapsulation of game messages into network command packets for multiplayer communication.

## Responsibilities
- Manages per-player command message queues
- Serializes game messages into network packets
- Handles packet fragmentation for large command sets
- Provides interfaces for adding/retrieving commands

## Key Types
- **CommandMsg (Class)**: Wrapper for game messages with timestamp and linking
- **CommandPacket (Struct)**: Network packet structure containing multiple commands
- **CommandPacketHeader (Struct)**: Header for command packets

## Key Functions
### AddToNetCommandList
- Purpose: Adds a game message to a player's command queue
- Calls: `NEW CommandMsg`, `SetPrevCommandMsg`, `SetNextCommandMsg`

### GetCommandMsg
- Purpose: Retrieves a game message from a player's command queue for current frame
- Calls: `GetNextCommandMsg`, `SetPrevCommandMsg`, `GetGameMessage`, `delete`

### AddCommandToPacket
- Purpose: Serializes game messages into a command packet
- Calls: `TheNetwork->queueSend`, `memcpy`

### GetCommandPacket
- Purpose: Returns the built command packet for network transmission
- Calls: None

## Globals
- **CommandHead[MAX_SLOTS] (CommandMsg*)**: Head pointers for per-player command queues
- **CommandTail[MAX_SLOTS] (CommandMsg*)**: Tail pointers for per-player command queues
- **commandBuf (unsigned char[])**: Buffer for building command packets
- **commandPacket (CommandPacket*)**: Pointer to command packet in buffer
- **bytesUsed (int)**: Tracks bytes used in current command packet

## Dependencies
- `Common/GameType.h`, `Common/MessageStream.h`, `Common/GameEngine.h`
- `GameLogic/GameLogic.h`, `GameNetwork/NetworkInterface.h`, `GameNetwork/NetworkDefs.h`
- `TheNetwork` (NetworkInterface instance)
- `DEBUG_LOG` macro
