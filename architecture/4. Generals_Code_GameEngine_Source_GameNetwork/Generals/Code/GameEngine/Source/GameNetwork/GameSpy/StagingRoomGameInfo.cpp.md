# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/StagingRoomGameInfo.cpp

## Purpose
Handles GameSpy-related game information and staging room functionality for multiplayer games.

## Responsibilities
- Manages GameSpy game slots and player information
- Handles local chat connection address resolution via SNMP
- Generates game results packets for GameSpy and ladder systems
- Manages game launch and network initialization
- Provides staging room functionality for multiplayer setup

## Key Types
- **tConnInfoStruct (Class)**: Represents TCP connection information (state, IP addresses, ports)
- **ConnInfoStruct (Class)**: Same as tConnInfoStruct (likely a typedef alias)
- **GameSpyGameSlot (Class)**: Extends GameSlot with GameSpy-specific player data (profile ID, wins/losses, etc.)

## Key Functions
### GetLocalChatConnectionAddress
- Purpose: Determines the local IP address used to connect to a GameSpy chat server
- Calls: gethostbyname, LoadLibrary, GetProcAddress, SnmpExtensionInitPtr, SnmpExtensionQueryPtr, SnmpUtilMemAllocPtr, SnmpUtilMemFreePtr

### GameSpyStagingRoom::startGame
- Purpose: Initializes and starts a GameSpy multiplayer game
- Calls: setLocalIP, NAT construction, TheGameSpyInfo methods, TheNAT methods

### GameSpyStagingRoom::generateGameSpyGameResultsPacket
- Purpose: Creates a GameSpy-formatted results packet after game completion
- Calls: TheVictoryConditions methods, TheNetwork methods, ThePlayerList methods

### GameSpyStagingRoom::launchGame
- Purpose: Finalizes game setup and launches the actual game
- Calls: NetworkInterface methods, TheMessageStream methods, TheWritableGlobalData methods

## Globals
- **SnmpExtensionInitPtr (Function pointer)**: Pointer to SNMP extension initialization function
- **SnmpExtensionQueryPtr (Function pointer)**: Pointer to SNMP query function
- **SnmpUtilMemAllocPtr (Function pointer)**: Pointer to SNMP memory allocation function
- **SnmpUtilMemFreePtr (Function pointer)**: Pointer to SNMP memory free function

## Dependencies
- GameSpy-specific headers (BuddyThread, PeerDefs, etc.)
- Networking headers (NAT, NetworkInterface)
- Game engine headers (GameState, Player, GameLogic)
- Common utilities (GameText, MapUtil)
- Windows SNMP API (inetmib1.dll, snmpapi.dll)
