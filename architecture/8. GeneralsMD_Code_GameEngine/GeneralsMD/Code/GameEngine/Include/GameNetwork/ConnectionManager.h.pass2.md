# GeneralsMD/Code/GameEngine/Include/GameNetwork/ConnectionManager.h - Enhanced Analysis

## Architectural Role
This file defines the central networking hub for the SAGE engine, managing all player connections, message routing, and synchronization logic. It acts as the intermediary between the game logic and the underlying transport layer, handling packet routing, reliability, and performance metrics.

## Cross-References
### Incoming
- **GameEngine**: Calls `init()`, `update()`, and `sendChat()` during game initialization and runtime.
- **UI/ChatSystem**: Uses `sendChat()` for in-game chat functionality.
- **FileTransferSystem**: Calls `sendFile()` and `getFileTransferProgress()` for mod asset distribution.
- **DisconnectManager**: Invokes `disconnectPlayer()` and `voteForPlayerDisconnect()` for player removal logic.

### Outgoing
- **Transport**: Delegates packet sending/receiving via `m_transport`.
- **FrameDataManager**: Manages frame synchronization per player (`m_frameData[MAX_SLOTS]`).
- **DisconnectManager**: Notifies of disconnections and votes (`m_disconnectManager`).
- **NetCommandWrapperList**: Handles command serialization/deserialization (`m_netCommandWrapperList`).

## Design Patterns
- **Facade Pattern**: Exposes high-level networking operations while hiding transport/connection complexity.
- **Observer Pattern**: Notifies subsystems (e.g., UI) of connection state changes (e.g., `processChat`).
- **Strategy Pattern**: Uses `m_packetRouterFallback` to dynamically switch routing strategies on failure.
