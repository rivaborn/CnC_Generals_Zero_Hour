# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpyGP.cpp

## Purpose
Handles GameSpy GP (Game Protocol) callbacks and utilities for buddy system and error management.

## Responsibilities
- Manages GameSpy connection and profile state
- Handles buddy message, status, and request callbacks
- Processes and logs GameSpy errors
- Provides reconnection logic for buddy system

## Key Types
- `GPConnection` (struct): GameSpy connection object
- `GPProfile` (type): GameSpy profile identifier
- `GPRecvBuddyMessageArg` (struct): Buddy message callback arguments
- `GPErrorArg` (struct): Error callback arguments
- `GPRecvBuddyStatusArg` (struct): Buddy status callback arguments
- `GPRecvBuddyRequestArg` (struct): Buddy request callback arguments

## Key Functions
### `GPRecvBuddyMessageCallback`
- Purpose: Handles incoming buddy messages
- Calls: `DEBUG_LOG`

### `buddyTryReconnect`
- Purpose: Attempts to reconnect to GameSpy chat server
- Calls: `TheGameSpyChat->reconnectProfile()`

### `GPErrorCallback`
- Purpose: Processes GameSpy errors and displays appropriate messages
- Calls: `DEBUG_LOG`, `GameSpyCloseOverlay`, `GSMessageBoxYesNo`

### `GPRecvBuddyStatusCallback`
- Purpose: Handles buddy status updates
- Calls: `DEBUG_LOG`

### `GPRecvBuddyRequestCallback`
- Purpose: Handles incoming buddy requests
- Calls: `DEBUG_LOG`

## Globals
- `TheGPConnectionObj` (GPConnection): Global GameSpy connection object
- `TheGPConnection` (GPConnection*): Pointer to global connection object
- `GameSpyLocalProfile` (GPProfile): Current GameSpy profile
- `GameSpyProfilePassword` (char[6
