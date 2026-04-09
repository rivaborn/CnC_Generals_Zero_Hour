# GeneralsMD/Code/GameEngine/Include/GameNetwork/LANAPI.h

## Purpose
Defines the LAN API interface and implementation for multiplayer communication in Command & Conquer Generals.

## Responsibilities
- Manages LAN broadcast communications
- Handles game joining/leaving, chat, and game options
- Maintains player and game lists
- Processes network messages and callbacks

## Key Types
- **LANAPIInterface (Class)**: Abstract interface for LAN API functionality
- **LANAPI (Class)**: Concrete implementation of LAN API
- **LANMessage (Struct)**: Message structure for LAN communication
- **ChatType (Enum)**: Types of chat messages (normal, emote, system)
- **ReturnType (Enum)**: Return codes for LAN operations
- **PendingActionType (Enum)**: Types of pending actions

## Key Functions
### RequestGameJoin
- Purpose: Request to join a game
- Calls: sendMessage

### RequestGameCreate
- Purpose: Try to host a game
- Calls: sendMessage

### RequestChat
- Purpose: Send a chat message
- Calls: sendMessage

### handleRequestJoin
- Purpose: Handle incoming join requests
- Calls: OnGameJoin, OnPlayerJoin

### handleChat
- Purpose: Process incoming chat messages
- Calls: OnChat

## Globals
- **g_lanPlayerNameLength (Int)**: Maximum player name length
- **g_lanMaxChatLength (Int)**: Maximum chat message length
- **m_lanMaxOptionsLength (Int)**: Maximum game options length

## Dependencies
- `GameNetwork/Transport.h`
- `GameNetwork/NetworkInterface.h`
- `GameNetwork/NetworkDefs.h`
- `GameNetwork/LANPlayer.h`
- `GameNetwork/LANGameInfo.h`
