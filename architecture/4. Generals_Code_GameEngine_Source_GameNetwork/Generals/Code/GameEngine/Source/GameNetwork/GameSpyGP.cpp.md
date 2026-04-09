# Generals/Code/GameEngine/Source/GameNetwork/GameSpyGP.cpp

## Purpose
Handles GameSpy GP (Game Protocol) callbacks and utilities for buddy system, error handling, and profile management.

## Responsibilities
- Manages GameSpy GP connection and callbacks
- Handles buddy messages, status updates, and requests
- Processes and displays GameSpy errors
- Maintains local profile and password state

## Key Types
- `GPConnection` (Class): GameSpy connection object
- `GPProfile` (Type): GameSpy profile identifier
- `GPRecvBuddyMessageArg` (Struct): Buddy message data
- `GPErrorArg` (Struct): Error information
- `GPRecvBuddyStatusArg` (Struct): Buddy status data
- `GPRecvBuddyRequestArg` (Struct): Buddy request data

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
- `TheGPConnectionObj` (GPConnection): Global connection object
- `TheGPConnection` (GPConnection*): Pointer to global connection
- `GameSpyLocalProfile` (GPProfile): Current user's profile
- `GameSpyProfilePassword` (char[64]): Password for
