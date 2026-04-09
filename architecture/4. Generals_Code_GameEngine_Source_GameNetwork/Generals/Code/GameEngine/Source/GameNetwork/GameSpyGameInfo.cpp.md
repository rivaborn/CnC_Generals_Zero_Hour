# Generals/Code/GameEngine/Source/GameNetwork/GameSpyGameInfo.cpp

## Purpose
Handles GameSpy-specific game setup, networking, and result reporting for multiplayer games.

## Responsibilities
- Manages GameSpy game slots and player info
- Initializes local network address via SNMP queries
- Launches and starts GameSpy games
- Generates game results packets for GameSpy servers

## Key Types
- `tConnInfoStruct` (Struct): Stores TCP connection state and addresses
- `ConnInfoStruct` (Struct): Same as above (typedef)
- `GameSpyGameInfo` (Class): Main class managing GameSpy game state

## Key Functions
### `GetLocalChatConnectionAddress`
- Purpose: Determines local IP used to connect to GameSpy chat server via SNMP
- Calls: `gethostbyname`, `LoadLibrary`, `GetProcAddress`, `SnmpExtensionInitPtr`, `SnmpExtensionQueryPtr`

### `GameSpyStartGame`
- Purpose: Initiates game start after validating minimum player count
- Calls: `TheGameSpyGame->startGame`

### `GameSpyLaunchGame`
- Purpose: Sets up network and launches the actual game
- Calls: `NetworkInterface::createNetwork`, `TheNetwork->init`, `TheNetwork->setLocalAddress`, `TheNetwork->attachTransport`

## Globals
- `TheGameSpyGame` (GameSpyGameInfo*): Singleton instance
- `SnmpExtensionInitPtr` (Function pointer): SNMP initialization function
- `SnmpExtensionQueryPtr` (Function pointer): SNMP query function
- `SnmpUtilMemAllocPtr` (Function pointer): SNMP memory allocation
- `SnmpUtilMemFreePtr` (Function pointer): SNMP memory deallocation

## Dependencies
- GameEngine headers (PreRTS, GameEngine, Player, etc.)
- GameSpy-specific headers (PeerDefs, GameSpyGameInfo)
- Networking headers (NetworkInterface, NAT)
- Common utilities (RandomValue, Scorekeeper)
