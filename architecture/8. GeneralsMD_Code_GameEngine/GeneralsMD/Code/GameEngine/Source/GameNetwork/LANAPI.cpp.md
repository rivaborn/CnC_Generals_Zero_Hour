# GeneralsMD/Code/GameEngine/Source/GameNetwork/LANAPI.cpp

## Purpose
Handles LAN communication for multiplayer gaming, including lobby management, game creation, and message routing.

## Responsibilities
- Manages LAN game sessions and player lobbies
- Handles message sending/receiving via UDP
- Maintains game and player lists
- Processes various LAN message types (joins, leaves, chat, etc.)
- Tracks game state and player connections

## Key Types
- **LANAPI (Class)**: Main LAN API class managing all LAN operations
- **LANMessage (Struct)**: Message container for LAN communication
- **LANGameInfo (Class)**: Represents a LAN game session
- **LANPlayer (Class)**: Represents a player in the lobby
- **Transport (Class)**: Handles low-level UDP transport

## Key Functions
### GetMessageTypeString
- Purpose: Converts message type ID to human-readable string
- Calls: None

### LANAPI::update
- Purpose: Processes incoming LAN messages and updates state
- Calls: handleRequestLocations, handleGameAnnounce, handleLobbyAnnounce, etc.

### LANAPI::sendMessage
- Purpose: Sends LAN messages to specific IP or broadcast
- Calls: m_transport->queueSend

### LANAPI::RequestSetName
- Purpose: Changes player name in lobby
- Calls: fillInLANMessage, sendMessage, addPlayer

### LANAPI::fillInLANMessage
- Purpose: Populates LAN message with local player info
- Calls: None

## Globals
- **lobbyPort (UnsignedShort)**: UDP port for LAN communication (8086)
- **LANbuttonPushed (Bool)**: External flag indicating UI button press
- **LANSocketErrorDetected (Bool)**: External flag for socket errors

## Dependencies
- Common/CRC.h, Common/GameState.h, GameNetwork/LANAPI.h
- GameNetwork/NetworkUtil.h, Common/GlobalData.h
- Common/RandomValue.h, GameClient/GameText.h
- GameClient/MapUtil.h, Common/UserPreferences.h
- GameLogic/GameLogic.h
