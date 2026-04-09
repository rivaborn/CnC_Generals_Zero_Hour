# GeneralsMD/Code/GameEngine/Source/GameNetwork/Network.cpp

## Purpose
Implements the Network singleton, handling multiplayer communication, command synchronization, and game state management.

## Responsibilities
- Manages network connections and message streams
- Synchronizes game commands across clients
- Handles player connections/disconnections
- Provides bandwidth metrics and load progress tracking

## Key Types
- **ConnectionMessage (struct)**: Encapsulates packet data and metadata for connection layer
- **Network (class)**: Singleton implementing NetworkInterface for game networking
- **None**: No other key types defined

## Key Functions
### `update()`
- Purpose: Main update loop for network processing
- Calls: `GetCommandsFromCommandList()`, `m_conMgr->update()`, `liteupdate()`, `AllCommandsReady()`, `RelayCommandsToCommandList()`

### `sendChat()`
- Purpose: Sends chat messages to other players
- Calls: `m_conMgr->sendChat()`

### `quitGame()`
- Purpose: Handles graceful game exit
- Calls: `m_conMgr->quitGame()`, `TheMessageStream->appendMessage()`

### `processRunAheadCommand()`
- Purpose: Updates run-ahead and frame rate settings
- Calls: `m_conMgr->setFrameGrouping()`

## Globals
- **NET_CRC_INTERVAL (Int)**: Interval for CRC checks (1 or 100)
- **CmdMsgLen (const int)**: Minimum command packet size (6 bytes)
- **TheNetwork (NetworkInterface*)**: Singleton instance

## Dependencies
- Key includes: `NetworkInterface.h`, `ConnectionManager.h`, `MessageStream.h`, `PlayerList.h`
- External symbols: `TheCommandList`, `TheGameLogic`, `TheWindowManager`, `TheRecorder`
