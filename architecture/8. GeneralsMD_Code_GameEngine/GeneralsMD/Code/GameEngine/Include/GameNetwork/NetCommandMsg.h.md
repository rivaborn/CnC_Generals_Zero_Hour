# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetCommandMsg.h

## Purpose
Defines network command message classes for the SAGE engine's multiplayer system.

## Responsibilities
- Declares base and derived NetCommandMsg classes for various network operations
- Provides message structures for game commands, acknowledgments, file transfers, chat, and disconnects
- Manages command execution timing and player associations
- Supports memory pooling for performance optimization

## Key Types
- **NetCommandMsg (Class)**: Base class for all network command messages
- **NetGameCommandMsg (Class)**: Represents game-specific messages with arguments
- **NetAckBothCommandMsg (Class)**: Combines stage 1 and 2 acknowledgment messages
- **NetChatCommandMsg (Class)**: Handles in-game chat messages
- **NetFileCommandMsg (Class)**: Manages file transfer data
- **NetWrapperCommandMsg (Class)**: Wraps large data chunks for transmission
- **NetCommandMsgMagicEnum (Enum)**: Magic number enum for message validation
- **NetCommandType (Enum)**: Not inferable (defined elsewhere)

## Key Functions
### NetGameCommandMsg::constructGameMessage
- Purpose: Creates a GameMessage from the command data
- Calls: Not inferable

### NetGameCommandMsg::addArgument
- Purpose: Adds an argument to the game message
- Calls: Not inferable

### NetWrapperCommandMsg::setData
- Purpose: Sets the wrapped data payload
- Calls: Not inferable

## Globals
- None

## Dependencies
- "Lib/BaseType.h" - Base types and memory management
- "GameNetwork/NetworkDefs.h" - Network type definitions
- "Common/UnicodeString.h" - Unicode string handling
- MemoryPoolObject - Base class for memory pooling
- GameMessage - External message class
- GameMessageArgument - External argument class
