# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/StagingRoomGameInfo.cpp

## Purpose
Handles GameSpy-specific staging room functionality for multiplayer games, including connection management, player info, and game launch.

## Responsibilities
- Manages GameSpy game slots and player info
- Handles local chat connection address resolution via SNMP
- Generates game results packets for GameSpy and ladder systems
- Launches games and manages NAT traversal
- Resets game state and manages player status

## Key Types
- **tConnInfoStruct (Class)**: Stores TCP connection info (state, IPs, ports)
- **ConnInfoStruct (Class)**: Same as tConnInfoStruct (likely a typedef alias)
- **GameSpyGameSlot (Class)**: Extends GameSlot with GameSpy-specific player data

## Key Functions
### GetLocalChatConnectionAddress
- Purpose: Determines the local IP address used to connect to a GameSpy chat server
- Calls: gethostbyname, LoadLibrary, GetProcAddress, SnmpExtensionInitPtr, SnmpExtensionQueryPtr, SnmpUtilMemAllocPtr, SnmpUtilMemFreePtr

### GameSpyStagingRoom::startGame
- Purpose: Initializes and starts a GameSpy game session
- Calls: setLocalIP, NAT constructor, TheGameSpyInfo methods, TheNAT methods

### GameSpyStagingRoom::generateGameSpyGameResultsPacket
- Purpose: Creates a GameSpy-formatted results packet after game completion
- Calls: TheVictoryConditions methods, TheNetwork methods, ThePlayerList methods

### GameSpyStagingRoom::launchGame
- Purpose: Finalizes game setup and launches the actual game
- Calls: NetworkInterface methods, TheNetwork methods, TheGameLogic methods, TheMapCache methods

## Globals
- **SnmpExtensionInitPtr (Function pointer)**: SNMP initialization function
- **SnmpExtensionQueryPtr (Function pointer)**: SNMP query function
- **SnmpUtilMemAllocPtr (Function pointer)**: SNMP memory allocation
- **SnmpUtilMemFreePtr (Function pointer)**: SNMP memory deallocation

## Dependencies
- GameState, Player, PlayerList, PlayerTemplate, RandomValue, ScoreKeeper
- GameText, MapUtil, Shell, GameLogic, VictoryConditions
- FileTransfer, BuddyThread, PeerDefs, PersistentStorageThread
- ThreadUtils, GameSpyOverlay, NAT, NetworkInterface
- PreRTS.h (must be first include)
