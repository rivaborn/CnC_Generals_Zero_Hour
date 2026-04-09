# GeneralsMD/Code/GameEngine/Source/GameNetwork/DisconnectManager.cpp - Enhanced Analysis

## Architectural Role
This file implements the core disconnection logic for multiplayer games, acting as the central coordinator for player timeouts, voting, and packet router transitions. It bridges the network layer (ConnectionManager) with the UI (DisconnectMenu) and game logic (GameLogic).

## Cross-References
### Incoming
- **GameNetwork/ConnectionManager.cpp**: Calls `update()` during network frame processing
- **GameClient/DisconnectMenu.cpp**: Triggers `voteForPlayerDisconnect()` via UI input
- **GameNetwork/NetworkInterface.cpp**: Dispatches disconnect-related commands to `processDisconnectCommand()`

### Outgoing
- **GameClient/DisconnectMenu.h**: Updates UI state via `TheDisconnectMenu->updateVotes()`
- **GameNetwork/ConnectionManager.h**: Manages player connections via `conMgr->disconnectPlayer()`
- **GameNetwork/GameSpy/PingThread.h**: Initiates ping requests for connectivity checks

## Design Patterns
- **Observer Pattern**: DisconnectManager monitors game frame progression and network state changes to trigger UI updates
- **State Pattern**: Uses `DISCONNECTSTATETYPE` enum to manage different disconnection states (SCREENOFF/SCREENON)
- **Command Pattern**: Encapsulates disconnect actions (votes, timeouts) as network commands (`NetCommandMsg` derivatives)
