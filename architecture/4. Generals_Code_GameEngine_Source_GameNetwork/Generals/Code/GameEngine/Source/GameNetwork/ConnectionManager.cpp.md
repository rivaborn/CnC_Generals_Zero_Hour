# Generals/Code/GameEngine/Source/GameNetwork/ConnectionManager.cpp

## Purpose
Manages network connections, command relaying, and game synchronization in multiplayer.

## Responsibilities
- Handles network transport and packet routing
- Manages command synchronization between players
- Processes network commands and relays them
- Tracks connection states and player status
- Manages file transfers and chat messages

## Key Types
- **ConnectionManager (Class)**: Main network manager class
- **NetCommandRef (Type)**: Reference to network commands
- **NetPacket (Class)**: Network packet container
- **FileCommandMap (Type)**: Maps file commands to paths

## Key Functions
### `doRelay()`
- Purpose: Processes incoming packets and relays commands to appropriate connections
- Calls: `processNetCommand`, `sendRemoteCommand`, `ackCommand`

### `sendChat()`
- Purpose: Sends chat messages to specified players
- Calls: `sendLocalCommand`, `processChat`

### `sendFileAnnounce()`
- Purpose: Announces file availability to other players
- Calls: `processFileAnnounce`, `sendLocalCommand`

### `updateLoadProgress()`
- Purpose: Updates and broadcasts load progress to other players
- Calls: `processProgress`, `sendLocalCommand`

### `notifyOthersOfCurrentFrame()`
- Purpose: Notifies other players of current game frame for synchronization
- Calls: `sendLocalCommandDirect`, `processDisconnectCommand`

## Globals
- **commandsReadyDebugSpewage (Int)**: Debug flag for command processing logging

## Dependencies
- Key includes: `ConnectionManager.h`, `Transport.h`, `NetCommandList.h`, `NetPacket.h`
- External symbols: `TheDisconnectMenu`, `TheLAN`, `TheGameLogic`, `TheLocalFileSystem`
