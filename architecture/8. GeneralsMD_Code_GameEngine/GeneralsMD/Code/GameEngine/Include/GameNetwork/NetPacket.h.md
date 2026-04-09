# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetPacket.h

## Purpose
Defines the `NetPacket` class for handling network message packets in the game.

## Responsibilities
- Manages packet data serialization/deserialization for network commands
- Handles packet size calculations and buffer management
- Supports various command types (game, ack, frame, chat, etc.)
- Provides packet construction and validation utilities

## Key Types
- **NetPacket (Class)**: Network packet handler with command serialization
- **NetPacketList (Class)**: List of NetPacket pointers
- **iterator (Class)**: Iterator for NetPacketList
- **NetPacketMagicEnum (Enum)**: Not inferable
- **NetPacket_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### `ConstructNetCommandMsgFromRawData`
- Purpose: Creates a NetCommandRef from raw packet data
- Calls: Not inferable

### `ConstructBigCommandPacketList`
- Purpose: Splits large commands into multiple packets
- Calls: Not inferable

### `GetBufferSizeNeededForCommand`
- Purpose: Calculates required buffer size for a command
- Calls: Not inferable

### `FillBufferWithCommand`
- Purpose: Serializes command data into packet buffer
- Calls: Not inferable

### `addCommand`
- Purpose: Adds a command to the packet
- Calls: Not inferable

### `dumpPacketToLog`
- Purpose: Debug function to log packet contents
- Calls: Not inferable

## Globals
- **MAX_PACKET_SIZE (const)**: Maximum packet size (defined elsewhere)

## Dependencies
- `NetworkDefs.h`
- `NetCommandList.h`
- `MessageStream.h`
- `GameMemory.h`
- `std::list`
- `MemoryPoolObject` (base class)
- `TransportMessage`
- `NetCommandRef`
- `NetCommandMsg`
- `GameMessage`
