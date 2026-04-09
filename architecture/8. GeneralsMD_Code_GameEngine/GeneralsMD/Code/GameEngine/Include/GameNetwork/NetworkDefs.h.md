# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetworkDefs.h

## Purpose
Defines core networking types, constants, and enums for the Command & Conquer Generals game engine.

## Responsibilities
- Declares packet structures (CommandPacket, TransportMessage)
- Defines network command types and flags
- Specifies connection limits and port numbers
- Exposes global network interface singleton

## Key Types
- **ConnectionNumbers (Enum)**: Player connection numbering (1-8 players + broadcast)
- **CommandPacket (Struct)**: Contains frame number, command count, and command data
- **TransportMessageHeader (Struct)**: Packet header with CRC and magic number
- **TransportMessage (Struct)**: Full transport layer message with header and payload
- **NetMessageFlag (Enum)**: Bit flags for message properties (ACK, sequenced, etc.)
- **NetCommandType (Enum)**: All network command types (game commands, chat, file transfer, etc.)
- **NetLocalStatus (Enum)**: Local player network states (pre-game, in-game, leaving, etc.)
- **PlayerLeaveCode (Enum)**: Reasons for player disconnection

## Key Functions
None (header-only file with no function definitions)

## Globals
- **WOL_NAME_LEN (Int)**: Maximum length for WOL (Westwood Online) names
- **MAX_COMMANDS (Int)**: Maximum commands per frame (256)
- **MAX_FRAMES_AHEAD (Int)**: External variable for runahead frames
- **MIN_RUNAHEAD (Int)**: Minimum runahead frames
- **FRAME_DATA_LENGTH (Int)**: Frame data buffer size
- **FRAMES_TO_KEEP (Int)**: Number of frames to keep in history
- **MAX_SLOTS (Int)**: Maximum player slots (8)
- **MAX_PACKET_SIZE (Int)**: Maximum packet size (476 bytes)
- **GENERALS_MAGIC_NUMBER (UnsignedShort)**: Packet identification magic number (0xF00D)
- **NETWORK_BASE_PORT_NUMBER (Int)**: Base port for network connections (8088)
- **TheNetwork (NetworkInterface**)**: Global network interface singleton

## Dependencies
- **Lib/BaseType.h**: Base types (Int, UnsignedInt, etc.)
- **Common/MessageStream.h**: Message stream definitions
- **NetworkInterface (Class)**: Forward declaration of network interface singleton
