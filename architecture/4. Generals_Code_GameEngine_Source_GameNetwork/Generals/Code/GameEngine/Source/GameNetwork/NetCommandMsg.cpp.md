# Generals/Code/GameEngine/Source/GameNetwork/NetCommandMsg.cpp

## Purpose
Implements network command message classes for the SAGE engine, handling game commands, acknowledgments, chat, file transfers, and progress reporting.

## Responsibilities
- Manages reference counting for message objects
- Constructs GameMessage objects from network data
- Handles various command types (game commands, acks, chat, files)
- Provides utility functions for player mask conversion

## Key Types
- **NetCommandMsg (Class)**: Base class for all network command messages
- **NetGameCommandMsg (Class)**: Handles game-specific commands with arguments
- **NetAckBothCommandMsg (Class)**: Acknowledgment message for two-stage confirmation
- **NetChatCommandMsg (Class)**: Handles in-game chat messages
- **NetFileCommandMsg (Class)**: Manages file transfer data

## Key Functions
### indexFromMask
- Purpose: Converts a player mask to a player index
- Calls: ThePlayerList->getNthPlayer(), player->getPlayerMask()

### NetGameCommandMsg::constructGameMessage
- Purpose: Creates a GameMessage from network command data
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
- GameMessage-related types and functions
