# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpyGameInfo.cpp

## Purpose
Handles GameSpy-specific game setup, networking, and result reporting for multiplayer games.

## Responsibilities
- Manages GameSpy game slots and player info
- Handles local chat connection address detection
- Initiates and launches GameSpy games
- Generates game results packets for GameSpy servers

## Key Types
- **tConnInfoStruct (Class)**: Stores TCP connection state and addresses
- **ConnInfoStruct (Class)**: Same as tConnInfoStruct (likely a typedef)
- **GameSpyGameInfo (Class)**: Main class managing GameSpy game state
- **GameSpyGameSlot (Class)**: Extends GameSlot with GameSpy-specific data

## Key Functions
### GetLocalChatConnectionAddress
- Purpose: Determines the local IP address used to connect to a GameSpy chat server
- Calls: gethostbyname, LoadLibrary, GetProcAddress, SnmpExtensionInitPtr, SnmpExtensionQueryPtr

### GameSpyStartGame
- Purpose: Initiates a GameSpy game if enough players are present
- Calls: TheGameSpyGame->startGame

### GameSpyLaunchGame
- Purpose: Sets up network infrastructure and launches the actual game
- Calls: NetworkInterface::createNetwork, TheNetwork->init, TheNetwork->setLocalAddress, TheNetwork->attachTransport

## Globals
- **TheGameSpyGame (GameSpyGameInfo*)**: Singleton instance of GameSpyGameInfo
- **SnmpExtensionInitPtr (function pointer)**: SNMP extension initialization function
- **SnmpExtensionQueryPtr (function pointer)**: SNMP query function
- **SnmpUtilMemAllocPtr (function pointer)**: SNMP memory allocation function
- **SnmpUtilMemFreePtr (function pointer)**: SNMP memory deallocation function

## Dependencies
- GameEngine.h, Player.h, PlayerList.h, RandomValue.h, Scorekeeper.h
- Shell.h, GameText.h, PeerDefs.h, GameSpyGameInfo.h, NetworkInterface.h
- NetworkUtil.h, NetworkDefs.h, NAT.h, GameLogic.h, VictoryConditions.h
