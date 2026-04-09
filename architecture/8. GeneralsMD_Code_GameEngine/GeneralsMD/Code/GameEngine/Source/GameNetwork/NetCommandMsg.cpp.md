# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetCommandMsg.cpp

## Purpose
Implements network command message classes for handling game commands, acknowledgments, chat, file transfers, and progress updates in the SAGE engine.

## Responsibilities
- Manages reference counting for network messages
- Handles game command serialization/deserialization
- Implements acknowledgment message types (stage 1, stage 2, both)
- Supports chat and file transfer messages
- Provides progress reporting mechanisms

## Key Types
- **NetCommandMsg (Class)**: Base class for all network command messages
- **NetGameCommandMsg (Class)**: Handles game-specific commands with arguments
- **NetAckBothCommandMsg (Class)**: Two-stage acknowledgment message
- **NetChatCommandMsg (Class)**: Chat message container
- **NetFileCommandMsg (Class)**: File transfer message
- **GameMessageArgument (Struct)**: Argument data container

## Key Functions
### indexFromMask
- Purpose: Converts a player mask to a player index
- Calls: ThePlayerList->getNthPlayer(), player->getPlayerMask()

### NetGameCommandMsg::constructGameMessage
- Purpose: Converts network command to executable GameMessage
- Calls: newInstance, ThePlayerList->findPlayerWithNameKey(), TheNameKeyGenerator->nameToKey(), retval->append*Argument()

### NetGameCommandMsg::addArgument
- Purpose: Adds an argument to a game command message
- Calls: newInstance

## Globals
- None

## Dependencies
- GameNetwork/NetCommandMsg.h
- Common/GameState.h
- Common/PlayerList.h
- Common/Player.h
- PreRTS.h
- GameMessage class and related types
