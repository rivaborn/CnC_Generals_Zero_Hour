# Generals/Code/GameEngine/Source/GameNetwork/LANAPI.cpp

## Purpose
Handles LAN communication for multiplayer gaming, including lobby management, game creation, and peer-to-peer messaging.

## Responsibilities
- Manages LAN game lobbies and game sessions
- Handles message routing and broadcasting
- Maintains player and game lists
- Provides utilities for IP resolution and message formatting

## Key Types
- `LANAPI` (Class): Main LAN API class managing all LAN operations
- `LANMessage` (Struct): Message container for LAN communication
- `LANGameInfo` (Class): Represents a LAN game session
- `LANPlayer` (Class): Represents a player in the lobby

## Key Functions
### `LANAPI::update`
- Purpose: Processes incoming LAN messages and updates transport layer
- Calls: `m_transport->update()`, `handleRequestLocations()`, `handleGameAnnounce()`, etc.

### `LANAPI::sendMessage`
- Purpose: Sends LAN messages to specific IPs or broadcasts
- Calls: `m_transport->queueSend()`

### `LANAPI::RequestSetName`
- Purpose: Changes the local player's name in the lobby
- Calls: `fillInLANMessage()`, `sendMessage()`

### `LANAPI::SetLocalIP`
- Purpose: Sets the local IP address for LAN communication
- Calls: `m_transport->reset()`, `m_transport->init()`

## Globals
- `lobbyPort` (UnsignedShort): UDP port used for LAN communication (8086)
- `LANbuttonPushed` (Bool): External flag indicating UI button state
- `LANSocketErrorDetected` (Bool): External flag for socket error state

## Dependencies
- Key includes: `PreRTS.h`, `Common/CRC.h`, `GameNetwork/LANAPI.h`, `GameNetwork/NetworkUtil.h`
- External symbols: `TheGlobalData`, `TheWritableGlobalData`, `OnChat`, `OnGameCreate`, `OnSlotList`, `OnNameChange`
