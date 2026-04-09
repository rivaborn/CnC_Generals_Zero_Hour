# Generals/Code/GameEngine/Source/GameNetwork/Network.cpp

## Purpose
Implements the Network singleton, handling multiplayer communication, command synchronization, and game state management.

## Responsibilities
- Manages network connections and message streams
- Synchronizes game commands across clients
- Handles player connections/disconnections
- Tracks bandwidth metrics and performance
- Manages file transfers and chat

## Key Types
- **ConnectionMessage (struct)**: Encapsulates packet data and metadata for connection layer
- **Network (class)**: Main network singleton implementing NetworkInterface
- **None**: No other key types defined

## Key Functions
### `update()`
- Purpose: Main network update loop processing commands and synchronization
- Calls: `GetCommandsFromCommandList`, `m_conMgr->updateRunAhead`, `liteupdate`, `AllCommandsReady`, `RelayCommandsToCommandList`

### `processCommand(GameMessage *msg)`
- Purpose: Processes incoming game commands
- Calls: `processFrameSynchronizedNetCommand`, `processRunAheadCommand`, `processDestroyPlayerCommand`

### `sendChat(UnicodeString text, Int playerMask)`
- Purpose: Sends chat messages to other players
- Calls: `m_conMgr->sendChat`

### `isFrameDataReady()`
- Purpose: Checks if next frame's data is ready for execution
- Calls: None

## Globals
- **NET_CRC_INTERVAL (Int)**: Interval for CRC checks (1 or 100 depending on debug mode)
- **CmdMsgLen (const int)**: Minimum command packet size (6 bytes)
- **TheNetwork (NetworkInterface*)**: Singleton instance of Network

## Dependencies
- Key includes: `NetworkInterface.h`, `ConnectionManager.h`, `MessageStream.h`, `Player.h`
- External symbols: `TheCommandList`, `TheGameLogic`, `ThePlayerList`, `TheWindowManager`, `TheScriptActions`, `TheScriptEngine`, `TheRecorder`, `TheGlobalData`
