# GeneralsMD/Code/GameEngine/Source/GameNetwork/Network.cpp - Enhanced Analysis

## Architectural Role
This file implements the core networking singleton, acting as the central coordinator for multiplayer communication. It bridges the game logic layer with the underlying transport layer (UDP), managing command synchronization, player management, and network state.

## Cross-References
### Incoming
- **GameLogic**: Calls `update()` and `liteupdate()` during game frame processing
- **Shell/Client**: Invokes `sendChat()` and `quitGame()` for UI-driven actions
- **Recorder**: Uses network state for replay synchronization

### Outgoing
- **ConnectionManager**: Delegates connection handling, file transfers, and player management
- **MessageStream**: Appends game messages for command synchronization
- **Udp/Transport**: Relies on underlying transport for packet routing

## Design Patterns
- **Singleton**: Ensures single network instance (`TheNetwork`)
- **Facade**: Hides transport complexity behind high-level API
- **Command Pattern**: Uses `GameMessage` objects for deferred command execution

*Not inferable*: Exact retry/acknowledgment strategy for unreliable UDP.
