# GeneralsMD/Code/GameEngine/Source/GameNetwork/LANAPI.cpp - Enhanced Analysis

## Architectural Role
This file implements the core LAN communication layer for multiplayer gaming, bridging the UI layer with the underlying UDP transport. It manages game lobbies, player lists, and message routing while handling connection state and timeouts.

## Cross-References
### Incoming
- GameClient UI components (e.g., lobby menu) call `RequestSetName`, `JoinGame`, `LeaveLobby`
- GameLogic may query `AmIHost()` for host privileges
- NetworkUtil likely calls `update()` during frame processing

### Outgoing
- Directly uses `Transport` class for UDP operations
- References `GameText` for localization and `MapUtil` for game setup
- Depends on `GlobalData` for game state persistence

## Design Patterns
- **Observer Pattern**: The `update()` loop processes incoming messages asynchronously
- **Resource Pooling**: Reuses `LANMessage` structs for message passing
- **State Machine**: Tracks connection states (lobby, in-game, inactive) with explicit transitions

*Not inferable*: Exact threading model or error recovery strategy.
