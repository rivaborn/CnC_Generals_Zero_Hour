# GeneralsMD/Code/GameEngine/Source/GameNetwork/FrameDataManager.cpp - Enhanced Analysis

## Architectural Role
This file implements the core frame-based networking synchronization mechanism in the SAGE engine. It manages the circular buffer of frame data used to track network commands for both local and remote players, enabling deterministic simulation across clients.

## Cross-References
### Incoming
- Networking subsystem (likely `GameNetwork/NetworkUtil.cpp`) calls `addNetCommandMsg` to enqueue commands
- Game logic (e.g., `GameLogic.cpp`) likely queries `allCommandsReady` and `getFrameCommandList` during simulation
- Connection management (e.g., `Connection.cpp`) probably uses `setQuitFrame` during game termination

### Outgoing
- Directly manipulates `FrameData` instances (circular buffer management)
- Uses `NetCommandMsg` and `NetCommandList` for command serialization
- Relies on `NetworkUtil.h` for frame arithmetic and constants

## Design Patterns
- **Circular Buffer**: Uses modulo arithmetic (`frame % FRAME_DATA_LENGTH`) to manage fixed-size frame history
- **Command Pattern**: Encapsulates network commands as `NetCommandMsg` objects for deferred execution
- **State Management**: Tracks command readiness per frame to synchronize simulation state across clients

*Not inferable*: Exact relationship with networking thread synchronization (likely handled elsewhere).
