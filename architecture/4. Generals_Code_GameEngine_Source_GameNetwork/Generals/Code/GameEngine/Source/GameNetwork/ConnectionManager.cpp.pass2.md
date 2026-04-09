# Generals/Code/GameEngine/Source/GameNetwork/ConnectionManager.cpp - Enhanced Analysis

## Architectural Role
Central hub for network synchronization in the SAGE engine, coordinating command relay, frame synchronization, and player connection management. Acts as the intermediary between the game logic and transport layer, ensuring consistent state across all connected clients.

## Cross-References
### Incoming
- **GameClient/DisconnectMenu.cpp**: Uses `ConnectionManager` for network state during disconnections
- **GameClient/InGameUI.cpp**: Queries connection status and FPS metrics
- **GameLogic/GameLogic.cpp**: Relies on frame synchronization via `notifyOthersOfCurrentFrame`
- **GameNetwork/NAT.cpp**: Uses connection routing for NAT traversal

### Outgoing
- **GameNetwork/Transport.cpp**: Delegates packet transmission via `m_transport`
- **GameLogic/ScriptEngine.cpp**: Processes script-triggered network commands
- **Common/Recorder.cpp**: Logs network events for replay systems
- **GameClient/MessageBox.cpp**: Displays connection-related UI messages

## Design Patterns
- **Observer Pattern**: Connection state changes notify multiple subsystems (e.g., UI updates via `TheDisconnectMenu`)
- **Command Pattern**: Network commands wrapped in `NetCommandRef` for deferred execution and relay
- **Singleton-like**: Global access via `TheConnectionManager` (implied by external references)
