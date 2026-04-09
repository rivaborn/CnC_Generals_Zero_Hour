# Generals/Code/Tools/mangler/wnet/tcp.cpp - Enhanced Analysis

## Architectural Role
This file implements the core TCP networking layer for the SAGE engine's multiplayer infrastructure, providing cross-platform socket abstraction for both client and server modes. It bridges low-level OS socket APIs with higher-level game networking systems.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wnet/tcp.cpp` (uses `ConnectAsync`, `EncapsulatedWrite`, `GetConnection`, `Wait`, `Write`, `WriteNB`)
- Likely called by game networking managers and matchmaking systems

### Outgoing
- Directly uses POSIX/Windows socket APIs (`socket`, `bind`, `connect`, `accept`, `select`)
- Depends on `Wtime` class for timeout handling
- Uses `fd_set` operations for socket multiplexing

## Design Patterns
- **Wrapper Facade**: Abstracts platform-specific socket APIs behind a unified interface
- **State Pattern**: Manages connection states (CLOSED, CONNECTING, CONNECTED) with explicit state transitions
- **Non-blocking I/O**: Uses `select()` and non-blocking sockets for asynchronous operations

*Not inferable: Exact usage patterns in game networking pipeline*
