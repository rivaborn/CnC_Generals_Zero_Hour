# Generals/Code/GameEngine/Source/GameNetwork/DisconnectManager.cpp

## Purpose
Manages player disconnections, timeouts, and voting in multiplayer games.

## Responsibilities
- Handles player disconnections and timeouts
- Manages disconnect voting system
- Coordinates packet router transitions
- Updates disconnect UI
- Sends keep-alive messages

## Key Types
- `DisconnectManager` (Class): Main class handling disconnections
- `DISCONNECTSTATETYPE` (Enum): Disconnect state types (SCREENOFF, SCREENON)
- `VoteInfo` (Struct): Stores vote information (vote flag and frame)

## Key Functions
### `update`
- Purpose: Updates disconnect state and checks for timeouts
- Calls: `turnOnScreen`, `sendKeepAlive`, `updateDisconnectStatus`, `nextFrame`

### `processDisconnectCommand`
- Purpose: Processes various disconnect-related network commands
- Calls: `processDisconnectKeepAlive`, `processDisconnectPlayer`, etc.

### `disconnectPlayer`
- Purpose: Disconnects a player and updates game state
- Calls: `TheDisconnectMenu->removePlayer`, `conMgr->disconnectPlayer`

### `voteForPlayerDisconnect`
- Purpose: Casts a vote to disconnect a player
- Calls: `sendVoteCommand`, `applyDisconnectVote`

### `allOnSameFrame`
- Purpose: Checks if all players are on the same frame
- Calls: None

## Globals
- `TheDisconnectMenu` (DisconnectMenu*): Reference to disconnect menu UI
- `TheGameLogic` (GameLogic*): Reference to game logic
- `TheNetwork` (NetworkInterface*): Reference to network interface
- `ThePinger` (PingThread*): Reference to ping thread
- `TheGameSpyConfig` (GSConfig*): Reference to GameSpy config

## Dependencies
- `DisconnectMenu.h`, `InGameUI.h`, `GameLogic.h`, `NetworkInterface.h`
- `NetworkUtil.h`, `PingThread.h`, `GSConfig.h`
- Uses `NetCommandMsg` and derived classes for network messages
