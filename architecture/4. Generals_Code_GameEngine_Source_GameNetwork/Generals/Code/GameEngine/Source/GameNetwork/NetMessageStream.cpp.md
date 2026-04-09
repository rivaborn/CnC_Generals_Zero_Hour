# Generals/Code/GameEngine/Source/GameNetwork/NetMessageStream.cpp

## Purpose
Handles encapsulation of game messages into network command packets for multiplayer communication.

## Responsibilities
- Manages per-player command message queues
- Serializes game messages into network packets
- Handles packet fragmentation for large command sets
- Provides interfaces for adding/retrieving commands

## Key Types
- CommandMsg (Class): Wraps a GameMessage with timestamp and linked-list pointers
- CommandPacket (Struct): Container for multiple game messages in a single network packet

## Key Functions
### AddToNetCommandList
- Purpose: Adds a GameMessage to a player's command queue
- Calls: NEW, DEBUG_LOG

### GetCommandMsg
- Purpose: Retrieves a GameMessage from a player's queue for the current frame
- Calls: DEBUG_LOG

### ClearCommandPacket
- Purpose: Initializes a new command packet for the current frame
- Calls: None

### AddCommandToPacket
- Purpose: Serializes a game message into the current command packet
- Calls: TheNetwork->queueSend, DEBUG_LOG

### GetCommandPacket
- Purpose: Returns the completed command packet for network transmission
- Calls: None

## Globals
- CommandHead[MAX_SLOTS] (CommandMsg*): Head pointers for per-player command queues
- CommandTail[MAX_SLOTS] (CommandMsg*): Tail pointers for per-player command queues
- commandBuf (unsigned char[]): Buffer for building command packets
- commandPacket (CommandPacket*): Pointer to the command packet in the buffer
- bytesUsed (int): Tracker for current packet size (used but not declared in shown code)

## Dependencies
- PreRTS.h, Common/GameType.h, Common/MessageStream.h, Common/GameEngine.h
- GameLogic/GameLogic.h, GameNetwork/NetworkInterface.h, GameNetwork/NetworkDefs.h
- TheNetwork (external symbol), GameMessage (external class)
