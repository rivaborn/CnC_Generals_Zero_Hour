# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetPacket.cpp

## Purpose
Handles network packet serialization/deserialization for game commands in the SAGE engine.

## Responsibilities
- Constructs NetCommandMsg objects from raw packet data
- Splits large commands into smaller packets for transmission
- Calculates buffer sizes for various command types
- Reads specific command message types from packet data

## Key Types
- NetPacket: Manages network packet data and command serialization
- NetCommandMsg: Base class for network command messages
- NetWrapperCommandMsg: Handles chunked command transmission

## Key Functions
### ConstructNetCommandMsgFromRawData
- Purpose: Parses raw packet data into a NetCommandMsg object
- Calls: readGameMessage, readAckBothMessage, etc. (one per command type)

### ConstructBigCommandPacketList
- Purpose: Splits large commands into smaller packets for transmission
- Calls: GetBufferSizeNeededForCommand, FillBufferWithCommand

### GetBufferSizeNeededForCommand
- Purpose: Calculates required buffer size for a command message
- Calls: GetGameCommandSize, GetAckCommandSize, etc. (one per command type)

### readChatMessage
- Purpose: Parses chat message data from packet
- Calls: None

### readWrapperMessage
- Purpose: Parses wrapper command data for chunked transmission
- Calls: None

## Globals
- None

## Dependencies
- GameNetwork/NetPacket.h
- GameNetwork/NetCommandMsg.h
- GameNetwork/NetworkDefs.h
- GameNetwork/NetworkUtil.h
- GameNetwork/GameMessageParser.h
- PreRTS.h
