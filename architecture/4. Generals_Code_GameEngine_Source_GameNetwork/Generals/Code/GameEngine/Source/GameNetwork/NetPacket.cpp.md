# Generals/Code/GameEngine/Source/GameNetwork/NetPacket.cpp

## Purpose
Handles serialization and deserialization of network packets for the game's networking layer.

## Responsibilities
- Parses raw network data into command messages
- Constructs packets from command messages
- Manages large packet fragmentation and reassembly
- Calculates packet size requirements for different message types
- Provides packet inspection utilities

## Key Types
- NetPacket (Class): Main packet handling class
- NetCommandMsg (Class): Base class for network commands
- NetCommandRef (Class): Reference wrapper for commands
- NetWrapperCommandMsg (Class): Handles fragmented packet reassembly

## Key Functions
### ConstructNetCommandMsgFromRawData
- Purpose: Parses raw network data into a command message
- Calls: readGameMessage, readAckBothMessage, etc. (message-specific parsers)

### ConstructBigCommandPacketList
- Purpose: Splits large commands into smaller packets for transmission
- Calls: GetBufferSizeNeededForCommand, FillBufferWithCommand

### GetBufferSizeNeededForCommand
- Purpose: Calculates required buffer size for a command message
- Calls: GetGameCommandSize, GetAckCommandSize, etc. (type-specific size calculators)

### readChatMessage
- Purpose: Parses chat message data from packet
- Calls: None (direct memory operations)

### dumpPacketToLog
- Purpose: Debug utility to log packet contents
- Calls: None

## Globals
- None

## Dependencies
- NetPacket.h, NetCommandMsg.h, NetworkDefs.h, NetworkUtil.h, GameMessageParser.h
- GameMessage, GameMessageParser, UnicodeString, AsciiString
- DEBUG_LOG_LEVEL, DEBUG_CRASH macros
